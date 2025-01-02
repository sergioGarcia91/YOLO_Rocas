# Modelos de redes neuronales convolucionales como herramienta para automatizar la clasificación de rocas

> García-Arias, S., y Velandia Patiño, F. A. (2025). Modelos de redes neuronales convolucionales como herramienta para automatizar la clasificación de rocas. Revista EIA, 22(43), 4317 pp. 1–28. DOI: https://doi.org/10.24050/reia.v22i43.1813 URL: https://revistas.eia.edu.co/index.php/reveia/article/view/1813

Este repositorio presenta modelos reentrenados de YOLO (YOLOv8n y YOLOv8x) diseñados para automatizar la identificación y clasificación de rocas ígneas, sedimentarias y metamórficas. Las etapas de entrenamiento se basaron en imágenes provenientes de Kaggle y del catálogo de la UIS, lo que permitió incorporar una mayor diversidad en las condiciones y la calidad de las imágenes utilizadas.


*Figura 4.	Validación final realizada al modelo “rocas_kuuku-x” utilizando muestras de la Escuela de Geología de la UIS. En la parte superior, A) las etiquetas originales de roca ígnea (color rojo), sedimentaria (color naranja) y metamórfica (color rosado). En la parte inferior, B) la predicción realizada por el modelo. La muestra en la fila 1, columna 2, es un ejemplo de una muestra con una predicción o etiqueta doble.*

<img src="https://github.com/sergioGarcia91/YOLO_Rocas/blob/dc048584a408f018bf9b87bbc754266c90cd5263/Fig_04.jpg" alt="Figura 4" width="400"/>

# Modelos
En el siguiente enlace de Drive se disponen los once modelos generados: https://drive.google.com/drive/folders/1u9ZhHxB7W6h5A4b4G3sV5qoR2HdmLrVd?usp=sharing

Las letras “k” y “u” representan el orden, de izquierda a derecha, en el que se utilizó cada catálogo durante el entrenamiento, donde “k” corresponde a Kaggle y “u” a UIS. El entrenamiento se llevó a cabo en varias etapas, generando diferentes modelos. El signo positivo en las épocas indica que estas son adicionales a las del modelo obtenido en la etapa previa.

| Modelo base YOLO      | Etapa | Modelo        | Épocas | Dataset |
|--------------|-------|----------------|--------|--------|
| YOLOv8n-seg  | 1     | rocas_k-n      | +100   | Kaggle |
|              | 2     | rocas_kk-n     | +60    | Kaggle |
|              | 3     | rocas_kku-n    | +103   | UIS    |
|              | 4     | rocas_kkuu-n   | +15    | UIS    |
|              | 5     | rocas_kkuuk-n  | +15    | Kaggle |
|              | 6     | rocas_kkuuku-n | +5     | UIS    |
| YOLOv8x-seg  | 1     | rocas_k-x      | +160   | Kaggle |
|              | 2     | rocas_ku-x     | +103   | UIS    |
|              | 3     | rocas_kuu-x    | +15    | UIS    |
|              | 4     | rocas_kuuk-x   | +15    | Kaggle |
|              | 5     | rocas_kuuku-x  | +5     | UIS    |

# Agradecimientos
Se agradece a la Escuela de Geología y al grupo de Geología Básica y Aplicada (GIGBA), Universidad Industrial de Santander por brindar acceso a parte del catálogo de rocas utilizado en el entrenamiento y la validación de los modelos.
