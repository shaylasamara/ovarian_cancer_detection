# Ovarian Ultrasound Image Classification Using EfficientNet-B3 and Transformer

## Project Overview

This project presents a hybrid deep learning framework for automated ovarian ultrasound image classification. The proposed system combines advanced image preprocessing, region-of-interest extraction, multi-scale feature learning, feature fusion, and Transformer-based contextual refinement to accurately classify ovarian ultrasound images into five clinically significant categories.

The primary goal is to assist healthcare professionals by providing a reliable computer-aided diagnostic system capable of distinguishing between normal and abnormal ovarian conditions from ultrasound scans.

---

## Problem Statement

Ovarian ultrasound interpretation is often challenging due to:

* Speckle noise and imaging artifacts
* Low contrast and blurry boundaries
* Similar visual appearance among ovarian conditions
* Operator-dependent image acquisition
* Variability in patient anatomy

Traditional diagnostic methods rely heavily on expert interpretation, which may introduce subjectivity and inconsistency. This project aims to address these challenges using a robust AI-based classification framework.

---

## Dataset

### Ovarian Ultrasound Images Dataset

* Total Images: **6,876**
* Image Type: Grayscale Ultrasound Images
* Classes: **5**

| Class             | Images |
| ----------------- | ------ |
| Healthy Ovary     | 1,464  |
| Dominant Follicle | 1,296  |
| Polycystic Ovary  | 1,422  |
| Simple Cyst       | 1,326  |
| Complex Cyst      | 1,368  |

Dataset Split:

* Training: 4,813 Images (70%)
* Validation: 1,031 Images (15%)
* Testing: 1,032 Images (15%)

---

## Proposed Framework

The framework consists of six major stages:

### 1. Image Preprocessing

* CLAHE Contrast Enhancement
* Morphological Filtering
* Normalization
* Data Augmentation

### 2. ROI Extraction

* U-Net Based Segmentation
* Region of Interest Identification

### 3. Multi-Scale Feature Extraction

* Pretrained EfficientNet-B3 Backbone
* Transfer Learning
* Multi-Level Feature Representation

### 4. Feature Fusion

* 1×1 Convolution
* Batch Normalization
* Multi-Scale Information Integration

### 5. Transformer Refinement

* 6 Transformer Encoder Layers
* 8 Attention Heads
* Self-Attention Mechanism
* Contextual Feature Learning

### 6. Classification

* Fully Connected Classification Head
* Five-Class Prediction

---

## Model Architecture

Input Ultrasound Image
↓
Preprocessing
↓
U-Net Segmentation
↓
EfficientNet-B3 Feature Extraction
↓
Multi-Scale Feature Fusion
↓
Transformer Encoder
↓
Classification Head
↓
Five-Class Ovarian Diagnosis

---

## Training Configuration

| Parameter          | Value      |
| ------------------ | ---------- |
| Optimizer          | AdamW      |
| Learning Rate      | 1e-4       |
| Weight Decay       | 1e-5       |
| Scheduler          | OneCycleLR |
| Loss Function      | Focal Loss |
| Alpha              | 0.25       |
| Gamma              | 2.0        |
| Epochs             | 50         |
| Transformer Layers | 6          |
| Attention Heads    | 8          |
| Early Stopping     | 5 Epochs   |

---

## Results

### Overall Performance

| Metric              | Score  |
| ------------------- | ------ |
| Test Accuracy       | 98.45% |
| Validation Accuracy | 98.55% |
| Precision           | 0.98   |
| Recall              | 0.98   |
| F1-Score            | 0.98   |

### Class-wise Performance

| Class             | Precision | Recall | F1-Score |
| ----------------- | --------- | ------ | -------- |
| Healthy Ovary     | 1.00      | 1.00   | 1.00     |
| Dominant Follicle | 1.00      | 1.00   | 1.00     |
| Polycystic Ovary  | 0.98      | 1.00   | 0.99     |
| Simple Cyst       | 0.99      | 0.94   | 0.97     |
| Complex Cyst      | 0.96      | 0.98   | 0.97     |

---

## Key Features

✔ Advanced Ultrasound Preprocessing

✔ U-Net Based ROI Segmentation

✔ Transfer Learning with EfficientNet-B3

✔ Multi-Scale Feature Fusion

✔ Transformer-Based Attention Mechanism

✔ Focal Loss for Better Class Learning

✔ High Classification Accuracy (98.45%)

✔ Medical AI Decision Support Framework

---

## Technologies Used

* Python
* PyTorch
* Torchvision
* OpenCV
* NumPy
* Pandas
* Scikit-Learn
* Matplotlib

---

## Future Improvements

* Clinical validation on larger datasets
* Explainable AI (Grad-CAM visualization)
* Vision Transformer (ViT) integration
* Real-time diagnostic deployment
* Multi-modal medical data fusion

---

## Conclusion

This project demonstrates the effectiveness of combining EfficientNet-B3 and Transformer architectures for ovarian ultrasound image classification. By integrating image preprocessing, segmentation, multi-scale feature extraction, feature fusion, and attention-based learning, the proposed framework achieves 98.45% test accuracy and shows strong potential as a computer-aided diagnostic tool for ovarian healthcare applications.
