# Problema 2

# Proyecto de Clasificación de Correos Spam con Regresión Logística

Este proyecto utiliza el dataset [Spambase](https://archive.ics.uci.edu/dataset/94/spambase) de UCI Machine Learning Repository para clasificar correos electrónicos como **spam** o **no spam**. El modelo empleado para la clasificación es la **regresión logística**, un enfoque simple y efectivo para problemas de clasificación binaria.

## Descripción del Proyecto

El objetivo del proyecto es entrenar un modelo que, dado el contenido de un correo electrónico, pueda predecir si dicho correo es spam o no. El dataset incluye varias características relacionadas con el contenido del correo, como la frecuencia de ciertas palabras y símbolos.

### Dataset

El dataset utilizado para este proyecto es el [Spambase Data Set](https://archive.ics.uci.edu/dataset/94/spambase) de UCI. Contiene 57 características extraídas de los correos electrónicos, y una columna objetivo que indica si el correo es spam (1) o no spam (0).

## Preguntas Clave

### a) Justificación del modelo utilizado

Se utilizó la **regresión logística** porque es un modelo de clasificación binaria que es simple de entrenar, interpretar y usar. Además, es adecuado cuando el número de muestras es suficientemente grande y las características se pueden escalar. En este caso, permite predecir si un correo es spam o no en función de las características del contenido del correo.

### b) ¿Qué características afectan más en que un correo sea Spam?

Para determinar qué características influyen más, se analizaron los coeficientes del modelo de regresión logística. Las 10 características más importantes son aquellas que tienen los coeficientes más grandes en valor absoluto. Estas características tienen un impacto más significativo en la predicción de si un correo es spam.

### c) Uso de métricas y su interpretación

A continuación, se explican las métricas utilizadas para evaluar el rendimiento del modelo y su interpretación:

- **Tasa de Error**: Es el complemento de la exactitud, es decir, el porcentaje de predicciones incorrectas.
  
- **Exactitud**: En este caso, la exactitud fue del **91.97%**, lo cual indica que la mayoría de las predicciones fueron correctas.
  
- **Matriz de Confusión**: La matriz de confusión nos da una idea clara de cómo el modelo está clasificando. En este caso, tenemos:
  - Verdaderos negativos (No spam correctamente identificado): 506
  - Falsos positivos (No spam identificado como spam): 25
  - Falsos negativos (Spam identificado como no spam): 49
  - Verdaderos positivos (Spam correctamente identificado): 341
  
- **Tasa de positivos verdaderos (Recall para spam)**: El modelo identificó correctamente el 87% de los correos que son spam.

- **Tasa de positivos falsos**: Representada por los falsos positivos en la matriz de confusión, que fue relativamente baja (25 casos).

- **Precisión**: La precisión de identificar correctamente los correos spam fue del **93%**.

- **F1-Score**: El **F1-Score** fue **0.9021**, lo que indica un buen equilibrio entre la precisión y el recall.

### Conclusión sobre las métricas

Para este caso, el **F1-Score** es una métrica importante ya que equilibra la precisión y el recall. Esto es relevante cuando el costo de los falsos negativos y falsos positivos es alto, como en la clasificación de spam, donde queremos minimizar tanto los correos importantes marcados como spam (falsos positivos) como los correos spam que pasan desapercibidos (falsos negativos).
