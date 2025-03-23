# Skin Cancer Detection System

## Overview
This project is a **Skin Cancer Detection System** that classifies skin images as **Benign, Malignant, Healthy Skin, or Not a Skin Image** using Machine Learning (ML) and Deep Learning (DL) techniques. The system features:

- **Feature Extraction**: Uses Contourlet Transform and Local Binary Pattern (LBP) for texture analysis.
- **ML Models**: Support Vector Machine (SVM) and Random Forest (RF) classifiers.
- **Deep Learning**: Uses VGG19 for feature extraction.
- **User Interface**: A **Streamlit**-based GUI for image upload and prediction.

---

## Dataset
The dataset consists of four categories:
1. **Benign** (Non-cancerous skin lesions)
2. **Malignant** (Cancerous skin lesions)
3. **Healthy Skin**
4. **Not a Skin Image** (Non-skin images for robustness)

Folder structure:
```
data/
 ├── train/
 │   ├── benign/
 │   ├── malignant/
 ├── test/
 │   ├── benign/
 │   ├── malignant/
 ├── healthy/
 ├── not_skin/
```

---

## Installation

### Prerequisites
Make sure you have Python installed. Then, install dependencies using:
```sh
pip install -r requirements.txt
```

---

## How to Run
### **1. Train the Model**
Run the script to train the model and save it:
```sh
python train.py
```
This will generate a `best_model.pkl` file.

### **2. Run the GUI**
Launch the Streamlit GUI with:
```sh
streamlit run gui.py
```

---

## Features & Functionality
- **Upload an image** (JPG, PNG, JPEG format)
- **Preprocessing**: Converts the image to grayscale and extracts features
- **Classification**: Predicts if the image is Benign, Malignant, Healthy, or Not a Skin Image
- **User-friendly interface** with Streamlit

---

## Issues & Fixes
### **Error: `FileNotFoundError: best_model.pkl not found`**
**Fix**: Ensure you have trained the model first by running:
```sh
python train.py
```

### **Error: `TypeError: list indices must be integers or slices, not numpy.float64`**
**Fix**: Convert `pred_label` to an integer before using it for indexing.

---

## Future Improvements
- Integration with **Deep Learning CNN models**
- Enhance dataset quality for better predictions
- Deploy as a **web-based API**

---
