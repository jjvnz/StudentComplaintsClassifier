# StudentComplaintsClassifier

## Descripción

Este proyecto emplea el modelo **DistilBERT** para la clasificación de quejas de estudiantes sobre la infraestructura universitaria. El objetivo es entrenar un modelo de aprendizaje automático capaz de identificar y clasificar quejas en diferentes categorías basadas en el contenido textual de las quejas.

## Estructura del Proyecto


```bash
StudentComplaintsClassifier/
│
├── data/
│   ├── university_students_complaints_es.csv
│   ├── university_students_complaints_labeled.csv
│   ├── university_students_complaints_train.csv
│   └── university_students_complaints_val.csv
│
├── scripts/
│   ├── label_data.py
│   ├── separete_dataset.py
│   ├── tokenizar.py
│   ├── train_model.py
│   └── evaluate_model.py
│
├── results/
│   └── evaluation_report.txt
│
├── train_dataset/
│
├── val_dataset/
│
└── fine-tuned-model/
    ├── config.json
    ├── model.safetensors
    ├── special_tokens_map.json
    ├── tokenizer_config.json
    ├── tokenizer.json
    └── vocab.txt

```


- **`scripts/`**: Contiene los scripts de Python para el procesamiento y entrenamiento.
  - **`label_data.py`**: Script para etiquetar los datos.
  - **`separete_dataset.py`**: Script para dividir los datos en conjuntos de entrenamiento y validación.
  - **`tokenizar.py`**: Script para tokenizar los datos utilizando el tokenizer de DistilBERT.
  - **`train_model.py`**: Script para entrenar el modelo DistilBERT con los datos tokenizados.
- **`data/`**: Contiene los archivos CSV con quejas.
  - **`university_students_complaints_es.csv`**: Archivo CSV con las quejas originales en español.
  - **`university_students_complaints_labeled.csv`**: Archivo CSV con las quejas etiquetadas.
  - **`university_students_complaints_train.csv`**: Archivo CSV con los datos de entrenamiento.
  - **`university_students_complaints_val.csv`**: Archivo CSV con los datos de validación.
- **`train_dataset/`**: Datos tokenizados para entrenamiento.
- **`val_dataset/`**: Datos tokenizados para validación.
- **`fine-tuned-model/`**: Contiene el modelo entrenado.
- **`results/`**: Contiene los resultados de la evaluación del modelo.
- **`README.md`**: Este archivo.
- **`requirements.txt`**: Archivo con los requisitos del proyecto.

## Requisitos

- **Python 3.7** o superior
- **transformers**
- **datasets**
- **pandas**
- **scikit-learn**

Instala los requisitos utilizando `pip`:

```bash
pip install transformers datasets pandas scikit-learn
```

## Instrucciones para Ejecutar el Proyecto

### 1. Preparar los Datos

1. Etiqueta tus datos ejecutando el script `label_data.py`.
2. Divide los datos en conjuntos de entrenamiento y validación.

### 2. Tokenizar los Datos

Ejecuta el script `tokenizar.py` para tokenizar los datos:

```bash
python3 tokenizar.py
```

### 3. Entrenar el Modelo

Ejecuta el script `train_model.py` para entrenar el modelo:

```bash
python3 train_model.py
```

### 4. Guardar el Modelo Entrenado

El modelo entrenado se guardará en el directorio `./fine-tuned-model`.

## Resultados

El modelo será evaluado durante el proceso de entrenamiento, y los resultados se guardarán en el directorio `./results`.


## Evaluación del Modelo

Después de entrenar el modelo, se realizó una evaluación utilizando el conjunto de validación. Los resultados fueron:

- **Precisión**: 1.00
- **Recall**: 1.00
- **F1-Score**: 1.00
- **Exactitud (Accuracy)**: 1.00

Estos resultados indican un rendimiento perfecto en el conjunto de validación. 

### Guardar el Modelo

El modelo entrenado se puede guardar para su uso futuro con los siguientes comandos:

```bash
python save_model.py
```

## Contribuciones

Las contribuciones son bienvenidas. Por favor, sigue estos pasos para contribuir:

1. Haz un fork del repositorio.
2. Crea una nueva rama (`git checkout -b feature/nueva-funcionalidad`).
3. Realiza tus cambios y haz commit (`git commit -am 'Añadir nueva funcionalidad'`).
4. Empuja los cambios a tu fork (`git push origin feature/nueva-funcionalidad`).
5. Crea un Pull Request.

## Licencia

Este proyecto está licenciado bajo la **Licencia MIT**. Consulta el archivo `LICENSE` para más detalles.

## Contacto

Si tienes preguntas o comentarios, puedes contactarme a través de [jjvnz.dev@outlook.com](mailto:jjvnz.dev@outlook.com).