# Predicción de reservas petroleras y evaluación de rentabilidad

Desarrollo de un sistema de selección de pozos petrolíferos basado en predicciones de reservas y análisis de riesgo. Con datos geológicos sintéticos de tres regiones, se entrena un modelo de Regresión Lineal para estimar el volumen de petróleo en nuevos pozos, se calcula la ganancia esperada para los 200 pozos más prometedores y se evalúa el riesgo asociado mediante bootstrapping.

## 🎯 Objetivos

* Predecir el volumen de reservas de nuevos pozos.
* Seleccionar los mejores 200 pozos por región según su volumen estimado.
* Determinar cuál región genera mayor beneficio económico.
* Evaluar riesgos y estabilidad usando bootstrapping (1,000 muestras, 95% CI).

## 🗂️ Datos

* `/datasets/geo_data_0.csv`
* `/datasets/geo_data_1.csv`
* `/datasets/geo_data_2.csv`

* `id` – identificador del pozo
* `f0`, `f1`, `f2` – características numéricas

## Metodología
* Preparación de datos
  * División train/test (75/25)
  * Escalado de características (StandardScaler)

* Entrenamiento del modelo
  * Regresión Lineal
  * Cálculo de RMSE y volumen promedio predicho por región

* Cálculo de beneficios
  * Selección de los 200 pozos con mayor volumen estimado
  * Evaluación de ingresos considerando:
    * $100M de inversión
    * $4,500 por unidad (1 mil barriles)

* Bootstrapping
  * 1,000 muestras por región
  * Intervalos de confianza del 95%
  * Cálculo de riesgo de pérdida


## 🧾 Conclusión

Aunque la región 0 muestra mayores ganancias iniciales, el análisis de riesgo mediante bootstrapping indica que la Región 1 es la única con riesgo inferior a 2.5%, lo que la convierte en la apuesta más segura y rentable bajo las condiciones del proyecto.
Los datos de exploración geológica de las tres regiones se almacenan en archivos:

  
