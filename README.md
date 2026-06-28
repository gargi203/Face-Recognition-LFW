# Face Recognition using Convolutional Neural Networks (CNN)

## Overview

This project implements a **Convolutional Neural Network (CNN)** for multi-class face recognition using the **Labeled Faces in the Wild (LFW)** dataset. The objective is to classify facial images of different individuals by learning discriminative facial features through deep learning.

The model is developed entirely from scratch using **TensorFlow/Keras**, without relying on pre-trained face recognition models, demonstrating the fundamentals of convolutional neural networks for image classification.

---

## Features

* Custom CNN architecture built using TensorFlow/Keras
* Face recognition on the LFW dataset
* Batch Normalization for faster convergence
* Dropout layers to reduce overfitting
* Data Augmentation for improved generalization
* Early Stopping and Model Checkpointing
* Learning Rate Scheduling with ReduceLROnPlateau
* Automatic saving of the best-performing model

---

## Dataset

**Labeled Faces in the Wild (LFW)** is a widely used benchmark dataset for face recognition.

* Dataset Source: Scikit-learn (`fetch_lfw_people`)
* Number of Classes: **7**
* Image Size: **50 × 37**
* Image Format: Grayscale
* Images are automatically normalized by the dataset loader.

---

## Model Architecture

The CNN consists of:

* Conv2D Layers
* Batch Normalization
* Max Pooling Layers
* Dropout Layers
* Global Average Pooling
* Fully Connected Dense Layer
* Softmax Output Layer

---

## Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook

---

## Training Configuration

| Parameter      |                                             Value |
| -------------- | ------------------------------------------------: |
| Optimizer      |                                              Adam |
| Learning Rate  |                                            0.0005 |
| Loss Function  |                   Sparse Categorical Crossentropy |
| Batch Size     |                                                32 |
| Maximum Epochs |                                                60 |
| Callbacks      | EarlyStopping, ModelCheckpoint, ReduceLROnPlateau |

---

## Results

| Metric                   |      Score |
| ------------------------ | ---------: |
| Best Validation Accuracy | **87.98%** |
| Best Validation Loss     | **0.3688** |

The model successfully learns discriminative facial features and achieves strong performance on the selected subset of the LFW dataset while maintaining good generalization through regularization techniques.

---

## Project Structure

```
Face-Recognition-LFW/
│
├── notebooks/
│   └── LFW_Face_Recognition.ipynb
│
├── models/
│   └── best_lfw_model.keras
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/gargi203/Face-Recognition-LFW.git
cd Face-Recognition-LFW
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter Notebook:

```bash
jupyter lab
```

or

```bash
jupyter notebook
```

---

## Future Improvements

* Increase image resolution for improved feature extraction
* Experiment with deeper CNN architectures
* Implement Transfer Learning using EfficientNet or ResNet
* Real-time face recognition using OpenCV
* Face verification using Siamese Networks
* Face embeddings with FaceNet or ArcFace


---

## License

This project is developed for educational and portfolio purposes.
