# **Siniestros_Viales-CABA**

![p](https://github.com/titolup/Siniestros_Viales-CABA/blob/main/Imagenes/Dise%C3%B1o%20sin%20t%C3%ADtulo%20(2).png)

Este proyecto, llevado a cabo bajo la simulación de un rol de Analista de Datos, tiene como objetivo principal realizar un análisis de datos solicitado por el Observatorio de Movilidad y Seguridad Vial (OMSV), que forma parte de la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires (CABA).

El propósito fundamental del proyecto es proporcionar información que permita tomar decisiones fundamentadas a las partes pertinentes, con el fin de prevenir accidentes, aumentar la seguridad vial y reducir los siniestros viales con víctimas fatales en la Ciudad de Buenos Aires.

Las tasas de mortalidad relacionadas con los siniestros viales son un indicador crítico de la seguridad vial en cualquier región. Estas tasas se calculan típicamente como el número de muertes por cada cierto número de habitantes o por cada cierta cantidad de vehículos registrados. La reducción de estas tasas es un objetivo primordial para mejorar la seguridad vial y proteger la vida de las personas en la ciudad.

Para lograr este objetivo, se utilizan datos iniciales obtenidos de un conjunto de datos que contiene información sobre los homicidios por siniestros viales en la Ciudad de Buenos Aires durante los años 2016-2021. Este conjunto de datos está disponible al público en la página oficial de CABA y puede accederse a través de los Datos Oficiales.

## **Contexto**

Los siniestros viales, también conocidos como accidentes de tráfico o accidentes de tránsito, son eventos que involucran vehículos en las vías públicas y que pueden tener diversas causas, como colisiones entre automóviles, motocicletas, bicicletas o peatones, atropellos, choques con objetos fijos o caídas de vehículos. Estos incidentes pueden tener consecuencias que van desde daños materiales hasta lesiones graves o fatales para los involucrados.

En Argentina, cada año mueren cerca de 4.000 personas en siniestros viales. Aunque muchas jurisdicciones han logrado disminuir la cantidad de accidentes de tránsito, esta sigue siendo la principal causa de muertes violentas en el país. Los informes del Sistema Nacional de Información Criminal (SNIC), del Ministerio de Seguridad de la Nación, revelan que entre 2018 y 2022 se registraron 19.630 muertes en siniestros viales en todo el país. Estas cifras equivalen a 11 personas por día que resultaron víctimas fatales por accidentes de tránsito.

Buenos Aires es la capital y ciudad más poblada de la República Argentina. La superficie de la Ciudad es algo superior a los 200 km2 y su perímetro, 60 km. Los habitantes que residen en ella, están distribuidos en barrios que, desde el punto de vista político-administrativo, se agrupan en quince comunas. La densidad de la población es de más de 15.000 habitantes por kilómetro cuadrado. Las zonas centro y norte son los espacios territoriales más densamente poblados.Página de la ciudad La población de la ciudad, según el Censo de 2022 es de 3 120 612 habitantes.Indec Solo en 2022, se contabilizaron 3.828 muertes fatales en este tipo de hechos. Los expertos en la materia indican que en Argentina es dos o tres veces más alta la probabilidad de que una persona muera en un siniestro vial que en un hecho de inseguridad delictiva.

Por todo ello, el estudio del problema para la prevención y disminución de Siniestros viales es escencialmente importante para las autoridades.

## **Actividades Desarrolladas**

[Datasets](https://github.com/titolup/Siniestros_Viales-CABA/tree/main/Datasets)

Para este proyecto, se trabajó con la Base de Datos de Víctimas Fatales en Siniestros Viales, la cual está en formato Excel y consta de dos pestañas:

**HECHOS:** En esta pestaña se registra cada incidente con un ID único, junto con las variables temporales, espaciales y de los participantes asociadas a cada uno.

**VICTIMAS:** Aquí se encuentra una fila por cada víctima de los incidentes, con información sobre su edad, sexo y modo de desplazamiento. Se establece una relación con la pestaña HECHOS a través del ID del incidente.

En este documento se proporcionan todas las definiciones pertinentes para el análisis de los datos y el desarrollo del proyecto. Además, los datos utilizados están disponibles en el siguiente enlace.

El proceso de ETL (Extracción, Transformación y Carga) implica la extracción y limpieza de datos de los conjuntos de datos HECHOS y VICTIMAS utilizando Pandas y Jupyter Notebook. Durante este proceso, se eliminan valores nulos y duplicados, se aplican transformaciones necesarias como cambios en los tipos de datos, eliminación de columnas no relevantes. [Link ETL](https://github.com/titolup/Siniestros_Viales-CABA/blob/main/1_ETL.ipynb)

Posteriormente, se lleva a cabo el Proceso de Análisis Exploratorio de Datos (EDA), una vez que los datos están limpios. En esta etapa, se exploran las relaciones entre las variables numéricas y categóricas de los conjuntos de datos. Se identifican posibles outliers o anomalías (que no necesariamente son errores), y se busca cualquier patrón o conocimiento que pueda ser útil en un análisis posterior. [Link EDA_Homicidios](https://github.com/titolup/Siniestros_Viales-CABA/blob/main/2_EDA_homicidios.ipynb) [Link EDA_Victimas](https://github.com/titolup/Siniestros_Viales-CABA/blob/main/3_EDA_victimas.ipynb)

## **Análisis de Datos**

**Análisis Temporal**

En el transcurso de los años, los accidentes con víctimas fatales muestran: para el período 2016-2018 una tendencia alta y estacionaria, que luego se convierte en bajista (teniendo en cuenta el comienzo de la Pandemia por COVID19 durante 2020); puede verse un pico de siniestros durante Diciembre de 2021 y se retoma la tendencia bajista. 

![a](https://github.com/titolup/Siniestros_Viales-CABA/blob/main/Imagenes/Captura%20de%20pantalla%20(75).png)

**Análisis Demográfico y Geográfico**

La distribución de la edad de las víctimas muestra que los hombres afectados generalmente se encuentran en el rango de edad de 20 a 40 años. Por otro lado, las mujeres afectadas tienden a estar en los rangos de 40, 60 y 80 años.

![e](https://github.com/titolup/Siniestros_Viales-CABA/blob/main/Imagenes/Captura%20de%20pantalla%20(72).png)

Utilizando la herramienta GeoPandas y extrayendo los datos de los detalles de las 15 comunas de CABA; resulta el análisis de las coordenadas geográficas y comunas de CABA, que demostro que las comunas con más siniestos son las 1, 4 , 9, 8 y 7.

![mapa](https://github.com/titolup/Siniestros_Viales-CABA/blob/main/Imagenes/Captura%20de%20pantalla%20(78).png)

Los siniestros se producen en 62% de los casos en el tipo de calle Avenida y en el 82% de los casos se corresponden con un Cruce entre calles. Lo que resulta un patrón que se repite a lo largo de los años. 

![c](https://github.com/titolup/Siniestros_Viales-CABA/blob/main/Imagenes/Captura%20de%20pantalla%20(76).png)

## **Indicadores de Rendimiento Clave KPI**

Una vez completado el Análisis Exploratorio de Datos, se utiliza el conjunto de datos resultante,junto con los datos extraídos de la página oficial de CABA que contienen información sobre las comunas. Estos datos se utilizan para desarrollar un tablero de Power BI con el objetivo de obtener los KPI (Indicadores Clave de Rendimiento) y un panel de presentación del informe con visualizaciones de datos.LINK foto dashboard kpi

Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior Se define la tasa de homicidios en siniestros viales como el número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico. Su fórmula es: (Número de homicidios en siniestros viales / Población total) * 100,000

Número de Homicidios de Siniestros = Tomando la variable Num víctimas del dataset Población Total = Tomada del Censo 2022. (Fuente:INDEC)

Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior Se define la cantidad de accidentes mortales de motociclistas en siniestros viales como el número absoluto de accidentes fatales en los que estuvieron involucradas víctimas que viajaban en moto en un determinado periodo temporal. Su fórmula para medir la evolución de los accidentes mortales con víctimas en moto es: (Número de accidentes mortales con víctimas en moto en el año anterior - Número de accidentes mortales con víctimas en moto en el año actual) / (Número de accidentes mortales con víctimas en moto en el año anterior) * 100

Cantidad de Accidentes Mortales en Moto = Tomando la variable Victima que se iguale a el campo MOTO del dataset

Reducir en un 15% la cantidad de accidentes con víctimas fatales de peatones en el último semestre, en CABA, respecto al semestre anterior. Se define la cantidad de accidentes fatales de peatones en siniestros viales como el número absoluto de accidentes fatales en los que estuvieron involucradas víctimas que circulaban a pie en un determinado periodo temporal. Su fórmula para medir la evolución de los accidentes mortales con víctimas peaton es: (Número de accidentes mortales con víctimas peaton en el semestre anterior - Número de accidentes mortales con víctimas peaton en el semestre actual) / (Número de accidentes mortales con víctimas peaton en el semestre anterior) * 100

Cantidad de Accidentes Mortales en Moto = Tomando la variable Victima que se iguale a el campo PEATON del dataset. Link foto KPI


## **Autor**
Este proyecto fue realizado por [Natalia Paez Marin]()
