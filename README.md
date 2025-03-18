# Práctica 19: 

Elaboró: Carlos Alejandro Jarero Gonzalez <al255813@alumnos.uacj.mx>

Matrícula: 255813

El presente Notebook fue relizado en equipo local con Kernel Python 3.11.8 en VS Code.

## Objetivos

El objetivo de esta actividad que el alumno haga un Exploratory Descriptive Analysis (EDA) y practicar .

## Instrucciones de uso

Este notebook puede extraer datos descargados directemente de un url.

Si quieres cambiar la fuente de datos solo ve a la sección de parameters y cambia el ```url```.

## Descripción del conjunto de datos

Utiliza el conjunto de datos "Haberman's Survival" disponible en el siguiente 'https://archive.ics.uci.edu/ml/machine-learning-databases/haberman/haberman.data"'. Este conjunto contiene datos de pacientes con cáncer de mama, incluyendo edad, año de operación, número de ganglios axilares y estado de supervivencia (categórico). El conjunto de datos tiene valores faltantes.

Puedes emplear este codigo para cargar tu codigo

```python
url = "https://archive.ics.uci.edu/ml/machine-learning-databases/haberman/haberman.data"
column_names = ['age', 'year', 'nodes', 'status']
data = pd.read_csv(url, header=None, names=column_names)
```

## Instrucciones para los estudiantes:

1. Descargar el archivo haberman.data desde el enlace proporcionado.

2. Realizar un EDA completo, incluyendo:

- Descripción de los datos.
- Histogramas para las columnas numéricas.
- Gráficas de barras para la columna categórica status (supervivencia).
- Boxplots para identificar outliers en las columnas numéricas.
- Matriz de correlación y mapa de calor.
- Pairplot para visualizar relaciones entre variables numéricas.
- Pruebas de normalidad (Shapiro-Wilk, Anderson-Darling, Kolmogorov-Smirnov) y QQplot para las columnas numéricas.

3. Identificar y tratar los datos faltantes utilizando técnicas como imputación por media, mediana o moda.

4. Repetir el EDA después del tratamiento de datos faltantes y comparar los resultados

5. Responde a estas preguntas y sube tus conclusiones a un PDF (se verificará el uso de IA)

A) Análisis Exploratorio de Datos (EDA):

- ¿Qué información relevante obtuviste de los histogramas y gráficas de densidad (PDF)? ¿Alguna variable parece seguir una distribución normal?
- ¿Qué insights obtuviste de las gráficas de barras para la variable categórica status? ¿Cómo se distribuyen los pacientes según su estado de supervivencia?

B) Pruebas de Normalidad:

- ¿Qué variables no siguen una distribución normal según las pruebas de Shapiro-Wilk, Anderson-Darling y Kolmogorov-Smirnov? ¿Cómo afecta esto al modelo de regresión lineal?
- ¿Qué conclusiones puedes extraer de los QQplots? ¿Qué variables tienen una distribución cercana a la normal?

C) Tratamiento de Datos Faltantes:

- ¿Qué columnas tenían todos los valores faltantes? ¿Cómo manejaste estas columnas?
- ¿Cómo cambió el EDA después de la imputación de datos? ¿Observaste diferencias significativas en las distribuciones de las variables?

D) Matriz de Correlación y Pairplot:

- ¿Qué relaciones lineales identificaste en la matriz de correlación y el pairplot? ¿Alguna variable tiene una correlación fuerte con la variable objetivo?
- ¿Cómo podrías utilizar esta información para seleccionar características (features) en un modelo de regresión lineal?
