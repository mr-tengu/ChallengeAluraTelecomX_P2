# 📡 Predicción de Churn de Clientes - Telecom X (Fase 2)

Este proyecto representa la segunda fase de la consultoría de datos para **Telecom X**. Tras haber realizado el proceso de ETL, en esta etapa nos enfocamos en el uso de **Machine Learning** para identificar patrones de evasión y predecir qué clientes tienen mayor probabilidad de cancelar sus servicios.

## 🎯 Propósito del Análisis
El objetivo principal es construir un modelo predictivo capaz de clasificar a los clientes en riesgo de **Churn** (cancelación). Al entender las variables que más influyen en esta decisión, la empresa puede implementar estrategias de retención proactivas y personalizadas.

## 📂 Estructura del Proyecto
* `TelecomX_Predictivo.ipynb`: Cuaderno de Google Colab con el flujo completo de ciencia de datos.
* `datos_tratados.csv`: Dataset limpio y transformado proveniente de la fase 1 (ETL).
* `visualizaciones/`: Carpeta que contiene los gráficos generados (Matriz de confusión, importancia de variables).
* `README.md`: Documentación del proyecto.

## ⚙️ Preparación de los Datos
Para que el modelo de aprendizaje automático pueda procesar la información, se realizaron las siguientes etapas:

1.  **Clasificación de Variables:**
    * **Numéricas:** `customer_tenure`, `account_Charges_Monthly`, `account_Charges_Total`.
    * **Categóricas:** `customer_gender`, `internet_InternetService`, `account_Contract`, entre otras.
2.  **Codificación (Encoding):** Se utilizó **One-Hot Encoding** para transformar las variables categóricas en binarias (0 y 1), permitiendo que el algoritmo interprete los datos de texto sin establecer una jerarquía falsa.
3.  **División del Dataset:** Los datos se separaron en:
    * **Entrenamiento (80%):** Para que el modelo aprenda los patrones de Churn.
    * **Prueba (20%):** Para evaluar la precisión del modelo con datos que nunca ha visto.

> **Justificación:** Se eligió el algoritmo **Random Forest** debido a su robustez frente a datos categóricos y su capacidad para explicar qué variables son las más importantes para la predicción.

## 📊 Insights y Visualizaciones Clave
Durante el Análisis Exploratorio de Datos (EDA) y el modelado, se obtuvieron los siguientes hallazgos:

* **Contrato Mes a Mes:** Es el predictor más fuerte de abandono. Los clientes sin compromiso anual tienen 5 veces más probabilidades de irse.
* **Fibra Óptica:** A pesar de ser un servicio premium, presenta una tasa de cancelación inusualmente alta, lo que sugiere problemas de precio o estabilidad técnica.



* **Matriz de Confusión:** El modelo demuestra una alta precisión para identificar a los clientes que se quedan, permitiendo enfocar los recursos de marketing solo en aquellos con alerta de salida.

## 🚀 Instrucciones de Ejecución
Para replicar este análisis en tu entorno local o en Google Colab, sigue estos pasos:

1.  **Instalación de Librerías:** Asegúrate de tener instalado Python 3.8+ y las siguientes dependencias:
    ```bash
    pip install pandas matplotlib seaborn scikit-learn
    ```
2.  **Carga de Datos:** Coloca el archivo `datos_tratados.csv` en la misma carpeta que el cuaderno.
3.  **Ejecución:** Abre `TelecomX_Predictivo.ipynb` y ejecuta todas las celdas en orden secuencial.

---
**Rol:** Analista de Datos / Data Scientist en formación  
**Fecha:** Marzo 2026
