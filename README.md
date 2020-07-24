# Comparación de modelos de deep learning para el conteo de multitudes

### :pencil2: Proyecto de Computer Vision - INF658

Este repositorio contiene el código fuente para entrenar los tres modelos comparados de CNN (CSRNet, LSC-CNN y SDC-Net).

***

**Realizado por:** Alain Alejo Huarachi y Ricardo Linares Juarez

**Profesor:** [Dr. Iván Sipirán Mendoza](//ivan-sipiran.com)

***

### :dvd: Conjunto de datos

[ShanghaiTech](//drive.google.com/open?id=16dhJn7k4FWVwByRsQAEpl9lwjuV03jVI)

### :pencil: CSRNet

1. Generar los ground truths: `make_dataset.ipynb`.
2. Entrenamiento: `python train.py train.json val.json 0 0`.
3. Pruebas: `val.ipynb`.

### :pencil: LCS-CNN

1. Instalar los requerimientos: `pip install -r requirements.txt`.
2. Colocar el dataset en la carpeta `dataset/` al mismo nivel que `lsc-cnn/`.
3. Descargar los [pesos entrenados de VGG](//https://drive.google.com/open?id=1hlJg4ux_BI3z_8zRdwwE7oQoumzSYIEg) (Colocar el folder `imagenet_vgg_weights/` al mismo nivel que `lsc-cnn/`).
4. Preparar el conjunto de datos: `python main.py --dataset="<parta|partb>" --gpu=<gpu_number>`.
5. Entrenamiento: `python main.py --dataset="<parta|partb>" --gpu=<gpu_number> --start-epoch=0 --epochs=30`.
6. Pruebas Parte A: `python main.py --dataset="parta" --gpu=<gpu_number> --start-epoch=13 --epochs=13 --threshold=0.21`.
6. Pruebas Parte B: `python main.py --dataset="partb" --gpu=<gpu_number> --start-epoch=24 --epochs=24 --threshold=0.25`
7. Resultados de validación: `models/dump`.
8. Resultados de pruebas: `models/dump_test`.

### :pencil: SDC-Net

### :page_facing_up: Requerimientos

* Python 3.8, Pytorch, Open CV, Numpy, Pandas, Myplotlib.
* Entornos recomendados:
    - JupyterLab.
    - Google Colaboratory.
    
### :file_folder: Documentación

* [Slides](//docs.google.com/presentation/d/1bFAN-F0g6dOkbWbD6fFEcdTUXP2bxbEt7kfYb3kzdI4/edit?usp=sharing).
* [Artículo](//www.overleaf.com/read/nqhmxddvjzbc).

