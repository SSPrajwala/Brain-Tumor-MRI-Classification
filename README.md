# Brain Tumor Classification from MRI Scans

## Project Overview

Early and accurate detection of brain tumors is critical for clinical decision-making and patient care. This project develops a deep learning pipeline for automatic brain tumor classification from MRI scans using both custom convolutional neural networks and transfer learning techniques.

The system classifies MRI images into four categories:

* Glioma
* Meningioma
* Pituitary Tumor
* No Tumor

The project emphasizes clinically relevant evaluation, explainable AI, and comparison between traditional CNN architectures and modern pretrained models.

---

## Dataset

Source: Brain Tumor MRI Dataset

Dataset Characteristics:

* Approximately 7,000 MRI images
* Four classification categories
* Preprocessed grayscale MRI scans
* Separate training and testing splits

Classes:

1. Glioma Tumor
2. Meningioma Tumor
3. Pituitary Tumor
4. No Tumor

---

## Objectives

* Build an end-to-end medical imaging classification pipeline
* Compare custom CNN and transfer learning approaches
* Apply medically appropriate data augmentation
* Evaluate models using clinical performance metrics
* Interpret model decisions using Grad-CAM visualizations
* Analyze the impact of class imbalance on medical predictions

---

## Medical Image Preprocessing

The preprocessing pipeline includes:

* Image resizing and normalization
* Intensity standardization
* Data augmentation
* Dataset balancing through class weighting

Medical imaging augmentation techniques:

✓ Rotation

✓ Horizontal Flip

✓ Zoom

✓ Brightness Adjustment

✗ Vertical Flip

✗ Unrealistic Distortions

These choices preserve anatomical realism while improving model generalization.

---

## Exploratory Data Analysis

The dataset was analyzed to understand:

* Class distribution
* Image quality
* Image dimensions
* Potential class imbalance

Key findings guided preprocessing decisions and class-weight calculations.

---

## Model Architectures

### Baseline CNN

Custom convolutional neural network containing:

* Convolutional Layers
* Batch Normalization
* Max Pooling
* Dropout Regularization
* Fully Connected Layers

Purpose:

* Establish a baseline benchmark
* Understand feature extraction fundamentals

---

### Transfer Learning: MobileNetV2

MobileNetV2 pretrained on ImageNet was used as a feature extractor.

Advantages:

* Efficient architecture
* Low parameter count
* Strong feature representation
* Fast inference performance

Training Strategy:

Phase 1:

* Frozen backbone
* Train classification head only

Phase 2:

* Fine-tune upper layers
* Lower learning rate
* Domain adaptation

---

## Training Strategy

Techniques used:

* Early Stopping
* Learning Rate Scheduling
* Model Checkpointing
* Class Weights
* Fine-Tuning

These methods improve generalization and reduce overfitting.

---

## Evaluation Metrics

The models were evaluated using clinically relevant metrics:

* Accuracy
* Precision
* Recall (Sensitivity)
* Specificity
* F1 Score
* ROC-AUC
* Confusion Matrix

Clinical metrics are particularly important because false negatives may have serious medical consequences.

---

## Explainable AI

Grad-CAM visualizations were used to interpret model predictions.

Benefits:

* Highlights important image regions
* Improves model transparency
* Supports clinical trust and interpretability
* Assists in understanding feature attention patterns

---

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* OpenCV
* Matplotlib
* Scikit-learn
* Jupyter Notebook

---

## Key Results

* Successfully classified four brain MRI categories.
* Transfer learning outperformed the baseline CNN.
* Class weighting improved minority-class recognition.
* Grad-CAM provided visual explanations for model predictions.
* Clinical evaluation metrics demonstrated model effectiveness.

---

## Future Improvements

* Incorporate MRI segmentation techniques.
* Train on larger multi-institutional datasets.
* Experiment with EfficientNet and Vision Transformers.
* Implement uncertainty estimation for clinical deployment.
* Develop a web-based diagnostic interface.

---

## Learning Outcomes

This project demonstrates:

* Medical Image Analysis
* Deep Learning
* Transfer Learning
* Computer Vision
* Explainable AI
* Model Evaluation
* Healthcare Analytics
* Clinical Machine Learning

---

## Author 
S S Prajwala
email: ssprajwala2023@gmail.com
github: https://github.com/SSPrajwala/Brain-Tumor-MRI-Classification
