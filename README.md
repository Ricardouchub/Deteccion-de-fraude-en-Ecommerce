# Detección de Fraude en E-commerce con Machine Learning


<p align="left">
  <img src="https://img.shields.io/badge/Proyecto_Completado-%E2%9C%94-2ECC71?style=flat-square&logo=checkmarx&logoColor=white" alt="Proyecto Completado"/>
  <img src="https://img.shields.io/badge/Python-3.9%2B-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/scikit--learn-Modelo_ML-F7931E?style=flat-square&logo=scikit-learn&logoColor=white" alt="scikit-learn"/>
</p>


Este repositorio contiene el desarrollo de un proyecto cuyo objetivo es construir un modelo de machine learning para detectar transacciones fraudulentas en una plataforma de e-commerce. A través de un análisis exploratorio detallado, una limpieza de datos  y la implementación de modelos avanzados como **Random Forest** y **XGBoost**, se logró desarrollar un clasificador con un **rendimiento perfecto (F1-Score de 1.0)**, validado rigurosamente mediante técnicas de validación cruzada para asegurar su fiabilidad y consistencia.

### [Notebook](https://github.com/Ricardouchub/Deteccion-de-fraude-en-Ecommerce/blob/main/Notebook.ipynb)
---

## Tabla de Contenidos
* [Problema de Negocio](#problema-de-negocio)
* [Dataset](#dataset)
* [Metodología](#metodología-del-proyecto)
* [Resultados Clave](#resultados-clave)
* [Tecnologías Utilizadas](#tecnologías-utilizadas)
* [Estructura del Repositorio](#estructura-del-repositorio)
* [Autor](#autor)

---

## Problema de Negocio

El fraude en transacciones online representa una de las mayores amenazas para las empresas de e-commerce, generando pérdidas millonarias, erosionando la confianza del cliente y aumentando los costos operativos por disputas y revisiones manuales. Este proyecto busca abordar este problema creando una solución automatizada que pueda:

1.  **Identificar transacciones fraudulentas** en tiempo real con alta precisión.
2.  **Minimizar los "falsos positivos"** para no afectar la experiencia de compra de clientes legítimos.
3.  **Proveer una solución escalable y automatizada** que fortalezca la seguridad financiera de la plataforma.

---

## Dataset

El proyecto utiliza el dataset **"Payment Fraud - Empowering Financial Security"** disponible en Kaggle. Contiene **38,662 transacciones** de e-commerce con 8 características, incluyendo la antigüedad de la cuenta, el método de pago, la categoría del producto y una etiqueta que indica si la transacción es legítima o fraudulenta.

**Fuente:** [Kaggle](https://www.kaggle.com/datasets/younusmohamed/payment-fraud-empowering-financial-security)

---

## Metodología del Proyecto

El proyecto se desarrolló siguiendo un ciclo de vida estructurado:

1.  **Limpieza y Preparación de Datos:** Se manejaron duplicados y valores nulos. Para estos últimos, se aplicó una estrategia de imputación avanzada con `IterativeImputer` para preservar la integridad de los datos sin descartar casos valiosos de fraude.

2.  **Análisis Exploratorio de Datos (EDA):** Se realizaron visualizaciones para entender la distribución de los datos y las relaciones entre variables. El hallazgo clave fue la identificación de una **correlación extremadamente fuerte entre las transacciones fraudulentas y su ocurrencia durante el fin de semana**, lo cual se convirtió en la principal variable predictiva.

3.  **Preprocesamiento:** Las variables categóricas se transformaron mediante One-Hot Encoding y las características numéricas fueron estandarizadas con `StandardScaler` para optimizar el rendimiento de los algoritmos.

4.  **Construcción y Evaluación de Modelos:** Se entrenaron y evaluaron tres modelos distintos (Regresión Logística, Random Forest y XGBoost), prestando especial atención al desbalance de clases mediante técnicas como `class_weight`, `SMOTE` y `scale_pos_weight`.

5.  **Validación de Robustez:** El modelo final (XGBoost) fue sometido a una **Validación Cruzada de 10 pliegues (10-Fold Cross-Validation)** para garantizar que su alto rendimiento era consistente y no producto de una división de datos afortunada.

---

## Resultados Clave

El modelo **XGBoost** se consolidó como la solución más eficaz, alcanzando un rendimiento perfecto y consistente.

* **F1-Score Promedio (Validación Cruzada):** **1.0000**
* **Desviación Estándar (Validación Cruzada):** **0.0000**

La matriz de confusión del modelo en el conjunto de prueba inicial muestra cero errores de clasificación:

<img width="550" height="423" alt="image" src="https://github.com/user-attachments/assets/235e5443-daf5-4ec8-a681-849ca94a8744" />


Este resultado excepcional confirma que el modelo aprendió a la perfección los patrones de fraude presentes en los datos, validando la efectividad del enfoque metodológico utilizado.

---

## Tecnologías Utilizadas
* **Lenguaje:** Python
* **Librerías Principales:**
    * Pandas & NumPy para manipulación de datos.
    * Scikit-learn para preprocesamiento, modelado y evaluación.
    * Imbalanced-learn para técnicas de manejo de desbalance.
    * XGBoost para el modelo de gradient boosting.
    * Matplotlib & Seaborn para visualización de datos.
    * Joblib para el guardado de modelos.

---

## Estructura del Repositorio
- **`Notebook.ipynb`**: Notebook principal del proyecto realizado.
- **`/modelos/`**: Carpeta que contiene los modelos entrenados.
- **`/data/`**: Carpeta que contiene el data set usado.
---


## Autor

**Ricardo Urdaneta** 

[**LinkedIn**](https://www.linkedin.com/in/ricardourdanetacastro)
