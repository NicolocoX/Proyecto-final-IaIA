# Proyecto-final-IaIA

Proyecto final del ramo de introducción a la inteligencia artificial

## Descripción del problema

La musicoterapia, o MT, es el uso de la música para mejorar el estrés, el estado de ánimo y la salud mental general de una persona. La MT también está reconocida como una práctica basada en pruebas, que utiliza la música como catalizador de hormonas de la «felicidad» como la oxitocina.

Sin embargo, la MT emplea una amplia gama de géneros diferentes, que varían de una organización a otra.

El objetivo del conjunto de datos MxMH es determinar si existe alguna correlación entre los gustos musicales de una persona y su salud mental. Idealmente, estos hallazgos podrían contribuir a una aplicación más informada de la MT o, simplemente, proporcionar interesantes visiones sobre la mente.

## Descripción del dataset

El dataset MXMH explora la relación entre las preferencias musicales de los individuos y su salud mental autoinformada. Contiene datos sobre género musical favorito, hábitos de escucha, estado emocional, niveles de ansiedad, depresión e insomnio, entre otras variables. Su objetivo es identificar posibles correlaciones entre el gusto musical y el bienestar psicológico, aportando información útil para la aplicación de la musicoterapia (MT) basada en evidencia. Este dataset contiene 736 muestras, donde cada una está descrita por 33 características.

[MXMH](https://www.kaggle.com/datasets/catherinerasgaitis/mxmh-survey-results?resource=download)

## Ordenamiento de datos y EDA

El código realiza una limpieza y transformación de datos que incluye la conversión de variables categóricas a numéricas, como por ejemplo transformar la variable "While working" de respuestas Sí/No a valores binarios 1/0. También elimina los valores nulos presentes en la columna 'Age' y mapea las frecuencias musicales categóricas ("Never", "Rarely", "Sometimes", "Very frequently") a valores numéricos del 0 al 3. Se eliminan además las columnas consideradas irrelevantes para el análisis. En la etapa de análisis visual, el código genera histogramas de variables numéricas clave como 'Age', 'Hours per day', 'Anxiety', entre otras, para observar sus distribuciones. Finalmente, se prepara un subconjunto de datos centrado en variables relacionadas con música y salud mental, identificando aquellas que serán útiles para un análisis posterior o para construir modelos predictivos.

## Clasificación K-Nearest Neighbors

De forma preliminar se utilizó un modelo K-Nearest Neighbors (KNN) combinado con una reducción de dimensionalidad mediante PCA a un solo componente. Sin embargo, este enfoque no se ajustó adecuadamente a los datos, ya que los resultados obtenidos fueron insatisfactorios y el modelo no logró realizar predicciones precisas. Debido a estas limitaciones, se decidió descartar este método para continuar explorando otras técnicas más adecuadas para el problema.

## Clasificación con Random Forest

Se utilizará Random Forest para clasificar la salud mental de los individuos a partir de sus gustos musicales. El dataset contiene 33 características, una cantidad que puede ser excesiva para algunos modelos, pero que Random Forest maneja sin problemas. Aunque la cantidad de datos no es alta, resulta adecuada para este tipo de modelo. Además, Random Forest destaca en clasificación multiclase y ofrece mayor precisión y robustez que un árbol de decisión individual.

## Metodología aplicada

1. Importación del dataset

2. Limpieza y preprocesamiento

3. Selección de características

4. Definición de la variable objetivo

5. División del conjunto de datos

6. Entrenamiento del modelo

7. Evaluación del modelo

8. Validación cruzada (opcional pero recomendable)

9. Tuning de hiperparámetros (opcional)

10. Interpretación y visualización de resultados

## Resultados obtenidos

## Conclusiones
