# ObjectDetection-using-Tensorflow

## Overview
This project demonstrates object detection using TensorFlow by training a Convolutional Neural Network (CNN) on the MNIST handwritten digit dataset. The model performs two tasks simultaneously:

- Classifies the handwritten digit (0–9).
- Predicts the bounding box surrounding the digit.

The project illustrates the concept of multi-output deep learning models by combining image classification and bounding box regression into a single neural network.

---

## Features

- Handwritten digit classification
- Bounding box prediction
- TensorFlow and Keras implementation
- Multi-output CNN architecture
- Data visualization with bounding boxes
- IoU (Intersection over Union) calculation
- Training and validation performance graphs

---

## Technologies Used

- Python
- TensorFlow
- TensorFlow Datasets (TFDS)
- NumPy
- Matplotlib
- Pillow (PIL)

---

## Dataset

The project uses the **MNIST** dataset available through TensorFlow Datasets.

The original 28×28 grayscale digit images are randomly placed on a 75×75 canvas. The model learns to:

- Identify the digit.
- Locate the digit by predicting its bounding box coordinates.

---

## Model Architecture

The CNN consists of:

### Feature Extraction
- Conv2D (16 filters)
- AveragePooling2D
- Conv2D (32 filters)
- AveragePooling2D
- Conv2D (64 filters)
- AveragePooling2D

### Dense Layers
- Flatten
- Dense (128 neurons)

### Output Layers
- Classification Output (Softmax, 10 classes)
- Bounding Box Regression Output (4 coordinates)

---

## Loss Functions

### Classification
- Categorical Crossentropy

### Bounding Box
- Mean Squared Error (MSE)

Optimizer used:

- Adam Optimizer

---

## Evaluation Metrics

- Classification Accuracy
- Bounding Box Mean Squared Error (MSE)
- Intersection over Union (IoU)

---

## Project Workflow

1. Load MNIST dataset
2. Generate random image positions
3. Create bounding box labels
4. Preprocess images
5. Train CNN model
6. Predict digit and bounding box
7. Evaluate model performance
8. Visualize predictions

---

## Results

The model predicts:

- Handwritten digit class
- Bounding box coordinates

The predicted bounding boxes are compared with the ground truth using IoU.

---

## Output

The project displays:

- Training images with bounding boxes
- Validation images with bounding boxes
- Classification accuracy
- Bounding box regression loss
- IoU values
- Prediction results

---

## Future Improvements

- Use deeper CNN architectures
- Improve bounding box accuracy
- Train on larger object detection datasets
- Implement real-time object detection
- Integrate YOLO or SSD models for advanced detection

---

Developed as part of a TensorFlow Object Detection project using Python and TensorFlow.
