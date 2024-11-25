
# Proyecto de Ciencia de Datos

## Resumen
Este proyecto consta de varias etapas de un pipeline de ciencia de datos, implementadas y documentadas en tres notebooks principales:
- Análisis Exploratorio de Datos (EDA)
- Desarrollo y Evaluación de Modelos
- Conclusiones Finales

---

## Notebooks

### 1. Análisis Exploratorio de Datos (EDA)
En este notebook, se derivaron patrones e insights clave del conjunto de datos. Aspectos destacados incluyen:
- Análisis de usuarios inactivos, enfocándose en cargos totales, cargos mensuales y tipo de contrato.
- Identificación de características significativas que influyen en la cancelación de contratos, como el tipo de contrato, donde aproximadamente el 90% de los usuarios inactivos tenían contratos mensuales.

**Preguntas Clave Planteadas:**
- ¿Por qué los registros de usuarios inactivos abarcan solo cuatro meses a pesar de tener datos de varios años?
- ¿Qué restricciones existen para la solución, como el tiempo de ejecución, tamaño del modelo o complejidad?
- ¿Debe el modelo proporcionar información sobre qué características influyen en la probabilidad de cancelación?

---

### 2. Desarrollo y Evaluación de Modelos
Este notebook incluye:
- Librerías utilizadas para el proyecto.
- Evaluación de modelos, incluyendo regresión logística.
- Métricas de evaluación detalladas para determinar el rendimiento de los modelos.

---

### 3. Conclusiones
El notebook de conclusiones resume el rendimiento de los modelos evaluados:
- **Random Forest**:
  - Precisión (1): 0.77, Recall (1): 0.57, F1-score (1): 0.66, ROC AUC: 0.7572
- **LightGBM**:
  - Precisión (1): 0.79, Recall (1): 0.63, F1-score (1): 0.70, ROC AUC: 0.7878
- **CatBoost** (Modelo Final):
  - Precisión (1): 0.82, Recall (1): 0.67, F1-score (1): 0.74, ROC AUC: 0.8126
- **Red Neuronal**:
  - Precisión (1): 0.67, Recall (1): 0.57, F1-score (1): 0.62, ROC AUC: 0.7377

**Selección del Modelo**: 
CatBoost fue seleccionado como el modelo final debido a su mejor desempeño en términos de recall (0.67) y F1-score (0.74) para la identificación de la clase positiva, minimizando los falsos negativos, lo cual es crucial en este contexto.

---

## Desafíos Clave
- Tiempos prolongados de ejecución durante la búsqueda de hiperparámetros, resueltos al identificar los valores óptimos.
- Preprocesamiento de datos, que requirió esfuerzos adicionales pero facilitó las etapas posteriores.

---

## Mejoras Futuras
- **Optimizar Recall**: Enfocarse en ajustar hiperparámetros o umbrales de clasificación para aumentar el recall.
- **Ajuste de Umbral**: Reducir el umbral de clasificación puede mejorar el recall a costa de la precisión.

---

Este README proporciona un resumen conciso del flujo de trabajo y los resultados del proyecto. Para más detalles, consulte los notebooks individuales.
