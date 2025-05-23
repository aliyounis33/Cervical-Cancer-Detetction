# Cervical-Cancer-Detetction

## Project Overview

This project focuses on the classification of cervical cell images using handcrafted features and classical machine learning techniques. The system was built to distinguish between normal, precancerous, and cancerous cervical cells using the SIPaKMeD dataset. The aim is to provide a computationally efficient solution that can perform well even in resource-limited environments.

## Dataset

* **Source:** SIPaKMeD (Single-cell Images for PAP Smear Analysis)
* **Classes:** Superficial-Intermediate, Parabasal, Koilocytotic, Dyskeratotic
* **Target Categories:** Normal, Precancerous, Cancerous

## Methodology

### 1. Image Preprocessing

* Extracted contours from `.dat` mask files
* Standardized image size to 48×62 with padding
* Generated binary masks for nucleus and cytoplasm

### 2. Feature Extraction

* **Color Intensity:** Mean R, G, B values for nucleus and cytoplasm
* **Morphology:** Circularity of nucleus and cytoplasm
* **Texture:**

  * HOG (Histogram of Oriented Gradients)
  * SIFT (Scale-Invariant Feature Transform, averaged descriptors)

### 3. Feature Selection

* **Filter Methods:** ANOVA F-test, Mutual Information
* Top features selected for training

### 4. Model Training and Evaluation

* **Models Used:** Decision Tree, Random Forest, SVM
* **Best Model:** Support Vector Machine (SVM)
* **Accuracy:** 85.6%
* **Evaluation Tools:** Confusion Matrix, ROC/AUC, Precision-Recall

## Requirements

* Python 3.7+
* OpenCV
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn

Install all dependencies with:

```bash
pip install -r requirements.txt
```

## How to Run

1. Preprocess the dataset using provided scripts
2. Run the feature extraction module
3. Apply feature selection methods
4. Train and evaluate models using `main.ipynb` or relevant scripts

## Contributions

* **Preprocessing:** Salah Mohamed
* **Feature Extraction:** Yasmine Mahmoud
* **Feature Selection:** Ali Younis
* **Model Training & Evaluation:** Abdelrahman Sayed Nasr
