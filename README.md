# SegundoProyecto
### Descripción del proyecto.
En este proyecto, realizamos un análisis exploratorio de datos para comprender y visualizar patrones, tendencias y características destacadas en nuestros datos. Se abordan aspectos clave como la búsqueda de valores faltantes, valores atípicos y registros duplicados.
## EDA
En todos los archivos que teniamos se hizo un Eda para tomar las decisiones adecuadas para nuestros KPI, aca unos ejemplos de los que se hizo.

df_accesotecnologia.head()
Este paso nos brinda una visión inicial de las primeras filas del conjunto de datos, ayudando a comprender su estructura.

df_accesotecnologia.info()
Proporciona detalles sobre las columnas presentes, los tipos de datos y la presencia de valores nulos.

df_accesotecnologia.describe()
Ofrece estadísticas descriptivas para las variables numéricas, proporcionando una comprensión más profunda de su distribución.

missing_values = df_accesotecnologia.isnull().sum()
Permite identificar la cantidad de valores faltantes en cada columna, si los hay.

duplicated_rows = df_accesotecnologia[df_accesotecnologia.duplicated()]
Muestra los registros duplicados en el conjunto de datos.

df_accesotecnologia = df_accesotecnologia.drop_duplicates()
Elimina los registros duplicados del conjunto de datos.

### Para el primer Kpi aumentar en un 2% el acceso al servicio de internet para el próximo trimestre, cada 100 hogares, por provincia.

Eliminación de Columnas sin Datos:
Se eliminan columnas sin datos en el DataFrame df_penetracion, creando un nuevo DataFrame llamado df_penetracion2.

Cambio de tipo de dato y reemplazo de comas:
La columna 'Accesos por cada 100 hogares' en df_penetracion2 se convierte a tipo numérico y se reemplazan las comas por puntos.
Concatenación de DataFrames:

Se concatenan los DataFrames df_penetracion2 y df_Baf en un nuevo DataFrame llamado df_concatenado.
se guarda el DataFrame Concatenado en un archivo CSV El DataFrame df_concatenado se guarda en un archivo CSV llamado 'concatenado.csv'.

Cálculo del KPI Propuesto:
Se carga el DataFrame desde el archivo CSV.
La columna 'Accesos por cada 100 hogares' se convierte a tipo numérico.
Se calcula el "Nuevo acceso" y el KPI propuesto para cada provincia.
Visualización del KPI Propuesto:

Se realiza una visualización de puntos que muestra la variación del acceso al servicio de Internet (con un aumento del 2%) por provincia.

El DataFrame con el KPI propuesto se guarda en un archivo CSV llamado 'Kpiconcatenado.csv', para el dashboard

### Para el segundo Kpi se hizo  aumento de la velocidad en 2% por trimestre
Se han cargado y concatenado varios conjuntos de datos relacionados con la velocidad de acceso a Internet.
Se eliminaron las columnas que no contenían datos para facilitar un análisis más preciso, se cálcula de la velocidad promedio trimestral, la visualización correspondiente y la implementación del KPI, así como la generación del archivo CSV para el dashboard
