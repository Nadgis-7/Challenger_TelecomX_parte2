# Challenger_TelecomX_parte2
# 📊 Proyecto Telecom X – Parte 2

## 🎯 Propósito del Análisis
El objetivo principal de este proyecto es **predecir la pérdida de clientes (Churn)** en la empresa ficticia **Telecom X**, utilizando variables relevantes obtenidas de datos demográficos, de uso de servicios y facturación.  
Este análisis busca identificar patrones y factores clave que influyen en la cancelación, con el fin de **reducir el churn y mejorar la retención de clientes**.

---

## 📁 Estructura del Proyecto

- **`Challenger_TelecomX_parte2.ipynb`** → Cuaderno principal con todo el análisis, preprocesamiento, modelado y conclusiones.
- **`/data`**
  - `datos tratados.csv` → Dataset procesado y listo para modelado.
- **`/visualizaciones`**
  - Gráficos generados en el EDA.
  - Curvas ROC y matrices de confusión de cada modelo.
- **`README.md`** → Este archivo descriptivo.

---

## 🧹 Preparación de Datos

### 📌 Clasificación de variables
- **Categóricas**: Tipo de contrato, método de pago, si tiene servicios adicionales, etc.
- **Numéricas**: Antigüedad (tenure), cargos mensuales, cargos totales.

### ⚙️ Procesamiento
1. **Estandarización** de variables numéricas (MinMaxScaler o StandardScaler según el modelo).
2. **Codificación** de variables categóricas (One-Hot Encoding).
3. **Balanceo de clases** utilizando **SMOTE** para manejar el desbalance entre clientes que cancelaron y los que permanecieron.

### 🔀 Separación de datos
- **Train**: 70%
- **Test**: 30%
- Justificación: esta división permite una evaluación equilibrada, garantizando datos suficientes para entrenamiento y validación.

---

## 🤖 Modelado

Se entrenaron y evaluaron **cuatro modelos**:

1. **Regresión Logística** → Interpretación directa de coeficientes.
2. **K-Nearest Neighbors (KNN)** → Basado en proximidad entre observaciones.
3. **Random Forest** → Importancia de variables calculada en base a reducción de impureza.
4. **Support Vector Machine (SVM)** → Separación óptima de clases mediante hiperplanos.

**Justificación de decisiones:**
- Se seleccionaron modelos con diferentes enfoques (lineales, basados en distancias, en árboles y en hiperplanos) para comparar rendimientos.
- Se utilizaron métricas como **Accuracy**, **ROC AUC**, **Precision**, **Recall** y **F1-score** para una evaluación completa.

---

## 📊 Ejemplos de Gráficos y Hallazgos del EDA

- Distribución de clientes por estado de cancelación (churn).
- Relación entre **Tenure** y probabilidad de cancelación.
- Comparación de **Cargos Mensuales** entre clientes que permanecen y los que cancelan.
- Curvas ROC para los cuatro modelos.
- Importancia de variables según cada algoritmo.

---

## ▶️ Instrucciones de Ejecución

### 1️⃣ Clonar repositorio
```bash
git clone https://github.com/Nadgis-7/Challenger_TelecomX_parte2.git
cd Challenger_TelecomX_parte2

## 2️⃣ Instalar dependencias
pip install -r requirements.txt
Bibliotecas necesarias:
(pandas==2.2.2
numpy==1.26.4
scikit-learn==1.4.2
matplotlib==3.8.3
seaborn==0.13.2
imbalanced-learn==0.12.2)

3️⃣ Ejecutar en Google Colab o localmente
Abrir Telecom_X_Parte2.ipynb.

Cargar el dataset procesado desde la carpeta /data.

Ejecutar las celdas en orden.
```
---
## 🙏 Agradecimientos
Este proyecto fue desarrollado como parte de la formación de **Alura + Oracle Next Education**.  
Agradezco profundamente la oportunidad de aprendizaje, el material brindado y el acompañamiento durante el proceso de desarrollo.




