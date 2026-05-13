# 🧠 Alzheimer's Disease Early Detection via MRI Classification

![Python](https://img.shields.io/badge/Python-3.8+-blue?logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-CNN%20%7C%20Hybrid-red?logo=tensorflow&logoColor=white)
![Accuracy](https://img.shields.io/badge/CNN%20Accuracy-98%25-brightgreen)
![Accuracy](https://img.shields.io/badge/Hybrid%20Accuracy-91%25-green)
![License](https://img.shields.io/badge/License-CC0--1.0-blue)
![Research](https://img.shields.io/badge/Research-Paper%20Published-blueviolet)

> Early detection of Alzheimer's disease from MRI scans using a CNN (98% accuracy) and a custom Hybrid model (91% accuracy) trained on the OASIS dataset — with a published research paper.

---

## 🧠 Problem Statement

Alzheimer's disease affects millions worldwide and is notoriously difficult to detect early. This project builds deep learning models to classify MRI brain scans into four stages of cognitive impairment, enabling earlier and more accurate diagnosis.

---

## 🏗️ Models

### 1. CNN Model — 98% Test Accuracy
A custom Convolutional Neural Network trained end-to-end on MRI images:
- Conv layers with ReLU activation
- MaxPooling for spatial downsampling
- Dropout for regularization
- Dense layers for 4-class classification

### 2. Hybrid Model — 91% Accuracy
A hybrid architecture combining CNN feature extraction with classical ML:
- CNN backbone for deep feature extraction
- Ensemble/classical layer for final classification
- Designed to test if traditional ML improves generalization over pure CNN

---

## 🗂️ Dataset

**Best Alzheimer's MRI Dataset** from Kaggle

| Class | Description |
|---|---|
| `No_Impairment` | Healthy brain — no signs of Alzheimer's |
| `Very_Mild_Impairment` | Earliest detectable stage |
| `Mild_Impairment` | Noticeable cognitive decline |
| `Moderate_Impairment` | Significant impairment |

**Dataset structure expected:**
```
data/
├── train/
│   ├── No_Impairment/
│   ├── Very_Mild_Impairment/
│   ├── Mild_Impairment/
│   └── Moderate_Impairment/
└── test/
    ├── No_Impairment/
    ├── Very_Mild_Impairment/
    ├── Mild_Impairment/
    └── Moderate_Impairment/
```

> Dataset is not included in this repo due to size. Download from [Kaggle — Best Alzheimer's MRI Dataset](https://www.kaggle.com/datasets/lukechugh/best-alzheimer-mri-dataset-99-accuracy) and place images in `train/` and `test/` folders as shown above.

---

## 📁 Project Structure

```
alzheimers-mri-classification/
│
├── CNN.ipynb                        # CNN model training and evaluation
├── HYBRID.ipynb                     # Hybrid model training and evaluation
├── train/                           # Training MRI images — download from Kaggle
├── test/                            # Test MRI images — download from Kaggle
├── Alzheimers Disease Paper.pdf     # Published research paper
├── Alzheimer's disease Report.pdf   # Full project report
├── requirements.txt
├── .gitignore
└── README.md
```

---

## 📊 Results

| Model | Test Accuracy | Notes |
|---|---|---|
| CNN | **98%** | Best performance, pure deep learning |
| Hybrid | **91%** | CNN + classical ML combination |

**Evaluation metrics used:**
- Accuracy
- Precision, Recall, F1-Score
- Matthews Correlation Coefficient (MCC)
- Confusion Matrix
- ROC-AUC (per class)

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| TensorFlow / Keras | CNN and Hybrid model building |
| NumPy + Pillow | Image loading and preprocessing |
| Scikit-learn | Metrics, evaluation, classical ML layers |
| Matplotlib + Seaborn | Visualization, confusion matrix, ROC curves |

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/sunilraj180805/alzheimers-mri-classification.git
cd alzheimers-mri-classification
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Download Dataset
Download from [Kaggle](https://www.kaggle.com/datasets/lukechugh/best-alzheimer-mri-dataset-99-accuracy) and place images in the `train/` and `test/` folders as shown in the structure above.

### 4. Run CNN Model
Open and run all cells in:
```
CNN.ipynb
```

### 5. Run Hybrid Model
Open and run all cells in:
```
HYBRID.ipynb
```

---

## 📄 Research Paper

This project was submitted as a research paper. The full paper is available in this repository:
📎 [`Alzheimers Disease Paper.pdf`](./Alzheimers%20Disease%20Paper.pdf)

---

## ⚠️ Limitations

- Models trained on this dataset — performance on other MRI formats may vary
- Grayscale MRI only — color or 3D volumetric scans require preprocessing changes
- Moderate Impairment class has fewer samples — slight class imbalance present

---

## 🔮 Future Scope

- 3D volumetric MRI classification using 3D-CNN or Vision Transformers
- Grad-CAM visualization to highlight disease-affected brain regions
- Clinical deployment as a screening tool with uncertainty estimation

---

## 👥 Team

- **Sunilraj D** — Model development, training pipeline, evaluation
- Aniketh Reddy — Repository management
- *(add other teammates and their roles)*

---

## 📜 License

This project is licensed under [CC0-1.0](LICENSE) — open for research and educational use.

---

## 🙋 Author

**Sunilraj D**
[GitHub](https://github.com/sunilraj180805)
