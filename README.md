# Enhancing Motor Imagery EEG Signal Classification Using Optimized CNN Architectures for Brain-Computer Interfaces

## Table of Contents

1. [Introduction](#introduction)
2. [Project Overview](#project-overview)
3. [Dataset](#dataset)
4. [Methodology](#methodology)
5. [Model Architectures](#model-architectures)
6. [Results](#results)
7. [Installation](#installation)
8. [Usage](#usage)
9. [Acknowledgements](#acknowledgements)
10. [License](#license)

---

## Introduction

This project focuses on enhancing Brain-Computer Interface (BCI) applications by improving the classification of Motor Imagery (MI) EEG signals. The study initially developed a Baseline CNN model as a starting point, evaluated multiple architectures, and selected the best-performing model for enhancement. The Enhanced CNN model was further optimized and extended for binary classification tasks.

---

## Project Overview

**Objective:**\
Design and analyze deep learning models based on CNNs to achieve accurate and reliable MI EEG signal classification.

**Key Features:**

- Baseline CNN development for benchmarking.
- Enhanced CNN models optimized for multi-class and binary classification tasks.
- Evaluation using the BCI Competition IV-2a dataset.

**Highlights:**

- Baseline CNN Accuracy: **40.00%** (Multi-class).
- Enhanced CNN Accuracy: **85.84%** (Multi-class).
- Binary Classification Accuracy:
  - **Feet vs Non-Feet - 96.43%**
  - **Left vs Non-Left - 96.82%**
  - **Right vs Non-Right - 97.97%**
  - **Tongue vs Non-Tongue - 97.78%**
- ROC-AUC: **1.00** (Binary Tasks).

---

## Dataset

**Source:** BCI Competition IV Dataset 2a.\
**Tasks:** Four Motor Imagery tasks:

- Left Hand, Right Hand, Both Feet, and Tongue.\
  **Participants:** 9 subjects with EEG recordings from 22 electrodes.

---

## Methodology

1. **Preprocessing:**
   - Artifact Removal using ICA.
   - Frequency filtering (8–30 Hz).
   - Data normalization and augmentation to enhance generalization.
2. **Model Development:**
   - Initial Baseline CNN model.
   - Selection and enhancement of the best-performing model.
   - Application of the enhanced model for binary classification tasks.
3. **Evaluation Metrics:**
   - Accuracy, F1-Score, and ROC-AUC.
   - 5-fold Stratified Cross-Validation.

---

## Model Architectures

### 1. Baseline CNN

- Simplified architecture for initial benchmarking.
- Accuracy: **40.00%** (Multi-class).
- Key Features: ReLU activation, max-pooling, and dropout for regularization.

### 2. DeepConvNet

- Deeper CNN for hierarchical feature extraction.
- Accuracy: **51.84%** (Multi-class).
- Key Features: Batch normalization and dropout layers for robustness.

### 3. Inception-like CNN

- Parallel convolutional layers for multi-scale feature extraction.
- Accuracy: **25.16%** (Multi-class).

### 4. ResNet-inspired CNN

- Introduces residual connections to address vanishing gradients.
- Accuracy: **24.00%** (Multi-class).

### 5. ShallowNet-like CNN

- Lightweight architecture with basic convolutional layers.
- Accuracy: **36.23%** (Multi-class).

### 6. EEGNet

- Lightweight and efficient architecture optimized for EEG data.
- Accuracy: **56.62%** (Multi-class).
- Key Features: Depthwise and separable convolutions.

### 7. Enhanced CNN (Best Performing Model)

- Optimized architecture integrating depthwise and separable convolutions.
- Accuracy: **85.84%** (Multi-class).
- Key Features: Robust feature extraction, dropout, and regularization for better generalization.

### 8. Enhanced Binary Classification Models

- Modified enhanced CNN applied to binary tasks:
  - **Feet vs Non-Feet:** Accuracy: **96.43%**, ROC-AUC: **1.00**.
  - **Left vs Non-Left:** Accuracy: **96.82%**, ROC-AUC: **1.00**.
  - **Right vs Non-Right:** Accuracy: **97.97%**, ROC-AUC: **1.00**.
  - **Tongue vs Non-Tongue:** Accuracy: **97.78%**, ROC-AUC: **1.00**.

---

## Results

**Multi-Class Classification:**

| Model                     | Accuracy (%) | Precision | Recall | F1-Score | ROC-AUC |
|---------------------------|--------------|-----------|--------|----------|---------|
| Baseline CNN              | 40.00        | 0.41      | 0.40   | 0.40     | 0.6328  |
| DeepConvNet               | 51.84        | 0.52      | 0.52   | 0.52     | 0.7762  |
| Inception-like CNN        | 25.16        | 0.32      | 0.25   | 0.14     | 0.5183  |
| ResNet-inspired CNN       | 24.00        | 0.08      | 0.25   | 0.12     | 0.5000  |
| ShallowNet-like CNN       | 36.23        | 0.38      | 0.36   | 0.36     | 0.6498  |
| EEGNet                    | 56.62        | 0.57      | 0.57   | 0.57     | 0.7948  |
| Enhanced CNN              | 85.84        | 0.86      | 0.86   | 0.85     | 0.9700  |

**Binary Classification:**

| Task                     | Accuracy (%) | Precision | Recall | F1-Score | ROC-AUC |
|--------------------------|--------------|-----------|--------|----------|---------|
| Feet vs Non-Feet         | 96.43        | 0.97      | 0.96   | 0.97     | 1.00    |
| Left vs Non-Left         | 96.82        | 0.97      | 0.97   | 0.97     | 1.00    |
| Right vs Non-Right       | 97.97        | 0.98      | 0.98   | 0.98     | 1.00    |
| Tongue vs Non-Tongue     | 97.78        | 0.98      | 0.98   | 0.98     | 1.00    |

---

## Installation

Clone the repository:

```bash
git clone https://github.com/username/repo-name.git](https://github.com/KaranShrestha16/Enhancing-Motor-Imagery-EEG-Signal-Classification-Using-Optimized-CNN-Architectures-for-BCI.git
```



## Acknowledgements

This project was conducted as part of the MSc in Data Science program at the University of Wolverhampton.\
**Supervisor:** Amin Noroozi Fakhabi\
**Student:** Karan Shrestha

---

## License

This project is licensed under the MIT License - see the LICENSE file for details.

