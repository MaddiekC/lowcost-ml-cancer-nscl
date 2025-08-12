# lowcost-ml-cancer-nscl

**Proyecto:** EVALUACIÓN COMPARATIVA DE MODELOS DE APRENDIZAJE AUTOMÁTICO DE BAJO COSTO PARA DIAGNÓSTICO DE CÉLULAS CANCEROSAS  
**Dataset:**  Dataset NSCL-Radiomics

Otros Repositorios 
- https://github.com/MaddiekC/lowcost-ml-cancer-cmmd.git
- https://github.com/DilanT123/lowcost-ml-cancer-padufes20.git
- https://github.com/DilanT123/lowcost-ml-cancer-cnn-extratrees.git
  
🧬 NSCLC-Radiomics: Pipeline de Procesamiento Multimodal
Este repositorio contiene la implementación completa de un pipeline de análisis multimodal para el conjunto de datos NSCLC-Radiomics , enfocado en la integración de datos clínicos, imágenes DICOM y características radiómicas para tareas de clasificación en cáncer de pulmón no microcítico (NSCLC).

El sistema realiza:

* Exploración y preprocesamiento robusto de datos
* Extracción optimizada de características de imágenes
* Selección de características (varianza, RFE, información mutua, etc.)
* Análisis de Componentes Principales (PCA)
* División y balanceo de datos (incluyendo SMOTE)
* Entrenamiento de modelos individuales con optimización de hiperparámetros
* Implementación avanzada de Ensemble Learning
* Evaluación final en conjunto de test

📁 Estructura del Proyecto

```
data/
├── NSCLC-Radiomics/                # Imágenes DICOM (LUNG1-XXX)
notebooks/                          # Análisis exploratorios (no mostrados en detalle)
src/
├── preprocessing.py
├── feature_extraction.py
├── feature_selection.py
├── pca_analysis.py
├── data_split.py
├── model_training.py
├── ensemble.py
├── evaluation.py
config/
├── config.yaml                     # Parámetros del pipeline
output/
├── resultados/
│   ├── exploration_results.json
│   ├── preprocessing_results.pkl
│   ├── image_extraction_metadata.json
│   ├── feature_selection_results.pkl
│   ├── pca_results.pkl
│   ├── data_split_results.pkl
│   └── model_comparison.png
├── modelos/
│   └── best_model_*.pkl
├── plots/
│   ├── confusion_matrix_*.png
│   └── preprocessing_results.png
logs/
├── processing.log
```

## 🚀 Cómo Empezar

### Prerrequisitos

Asegúrate de tener Python 3.8+ instalado. Puedes instalar todas las dependencias necesarias ejecutando:

```bash
pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn plotly pydicom pyyaml xgboost
```

### Configuración

1.  **Clona el repositorio:**
    ```bash
    git clone https://github.com/MaddiekC/lowcost-ml-cancer-cmmd.git
    cd lowcost-ml-cancer-cmmd
    ```

2.  **Descarga los datos:**
    Descarga el dataset NSCLC y colócalo en la carpeta `data/` siguiendo la estructura mencionada arriba.

3.  **Configura el pipeline:**
    Abre el archivo `config.yaml` para ajustar las rutas de los ficheros, los parámetros del modelo y las etapas del pipeline que deseas ejecutar.

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Si tienes alguna idea para mejorar el proyecto, por favor abre un "issue" para discutirlo o envía directamente un "pull request".

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.

