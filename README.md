# The caries detection web-service using the YOLOv11 neural network

**Author - Prathviraj Gawali**

This repository contains the YOLOv11 object detection web service, that detects caries and other teeth deceases on images. Also, it contains additional scripts, that can be used to prepare the source dataset, to train the model and run test predictions.

The DentalAI dataset used to train the model. You can download it from here: https://datasetninja.com/dentalai. If you want to run your own training process, you need to convert it to the YOLOv8 format, using the script in the `convert.ipynb` notebook.

This is a source code for the **Teeth caries detection using YOLOv11.Nano neural network**. 

## Contents

* `convert.ipynb` - The Supervisely to YOLOv11 converter, used to convert the dataset to YOLOv11 format
* `train.ipynb` - The code to train the YOLOv11 model using converted dataset
* `predict.ipynb` - The code, that can be used to run and visualize caries detection on custom images, using the trained model
* `best.pt` - The trained YOLOv11 model on 30 epochs to detect caries, cavity and cracks on teeth
* `object_detector.py` - The backend of a web service
* `index.html` - The frontend of a web service
* `caries.jpg` - Sample teeth with caries image

## Steps
1. When to open in Jupyter Notebook
    1) Open Virtual Env
        ```bash
        .\venv\Scripts\Activate.ps1
        ```
    2) Open Juputer Notebook 
        ```python
        python -m notebook
        ```
2. Run As webservices
    ```python
        python object_detector.py
    ```


## Run web service

* Ensure that the `object_detector.py`, `index.html` and `best.pt` files located in the same folder
* Run

```
python object_detector.py
```

The web interface will be available on **http://localhost:8080** address. You can upload the teeth image and see if it contains caries.
