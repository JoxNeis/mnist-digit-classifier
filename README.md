# 🧠 MNIST Digit Classifier (CNN)

A **Convolutional Neural Network (CNN)** model for handwritten digit classification using an MNIST-style image dataset.

This project demonstrates a full deep learning workflow including:

* Data extraction
* CNN model training
* Model evaluation
* Confusion matrix visualization

## 📌 Project Overview

This project builds a **digit classification model** that predicts handwritten digits (0–9) from images.

The workflow includes:

1. Load dataset from ZIP file
2. Preprocess images using normalization
3. Train CNN model
4. Evaluate model performance
5. Visualize predictions using confusion matrix

## 🗂 Repository Structure

```bash
mnist-digit-classifier/
│
├── HandwrittingClassifier.ipynb   # Main notebook
├── mnist.zip                      # Dataset (not recommended to upload if large)
├── README.md                      # Project documentation
```

## 📦 Dataset

The dataset is stored in:

```bash
mnist.zip
```

After extraction:

```bash
mnist_dataset/
├── train/
├── test/
```

Each folder contains digit images labeled **0–9**.

## 🧠 Model Architecture

The model uses a **Convolutional Neural Network (CNN)**.

## Architecture Summary

```text
Input: (224, 224, 3)

Conv2D (32 filters, 3x3, ReLU)
MaxPooling2D (2x2)

Conv2D (64 filters, 3x3, ReLU)
MaxPooling2D (2x2)

Conv2D (128 filters, 3x3, ReLU)
MaxPooling2D (2x2)

Flatten

Dense (128, ReLU)

Dropout (0.0)

Dense (10, Softmax)
```

---

## 🏋️ Training Configuration

Model compilation:

```python
optimizer = 'adam'
loss = 'categorical_crossentropy'
metrics = ['accuracy']
```

Training:

```python
epochs = 10
```

Validation is performed during training.

## 📊 Evaluation

Model evaluation includes:

* Accuracy measurement
* Confusion matrix
* Classification report

Implemented using:

```python
sklearn.metrics:
- confusion_matrix
- classification_report
- ConfusionMatrixDisplay
```

---

## Visualization

Training performance visualization includes:

* Accuracy graph
* Loss graph
* Confusion matrix

Libraries used:

```python
matplotlib
numpy
```
