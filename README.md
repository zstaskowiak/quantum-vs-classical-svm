# 🧠 Quantum vs Classical Support Vector Machine (QSVM vs SVM)
 
**Project title:** Quantum Support Vector Machine for Big Data Classification  
**Tools:** Qiskit · Scikit-learn · NumPy · Python  
**Dataset:** Breast Cancer Wisconsin (Diagnostic)  

---

## 📖 Overview

This project explores and compares **Quantum Support Vector Machines (QSVM)** and **Classical Support Vector Machines (SVM)** on the **Breast Cancer Wisconsin (Diagnostic)** dataset.  
While classical SVMs use traditional kernel functions to find optimal separating hyperplanes, QSVMs leverage **quantum feature maps** and **quantum kernels** to operate in a high-dimensional **Hilbert space**.

By exploiting quantum principles such as **superposition** and **entanglement**, QSVMs aim to enhance classification performance for complex, non-linear data — though current quantum simulators still face scalability and noise limitations.

---

## 🎯 Objectives

- Implement both **classical SVM** and **quantum SVM** models.  
- Compare their **accuracy and computational performance**.  
- Explore the **potential and limitations** of quantum-enhanced machine learning.  
- Evaluate how PCA affects model training speed and accuracy.

---

## ⚙️ Tech Stack

| Category | Tools |
|-----------|--------|
| Language | Python |
| Quantum Framework | Qiskit, Qiskit Machine Learning |
| ML Libraries | Scikit-learn |
| Data Handling | NumPy, PCA, MaxAbsScaler |
| Evaluation | Accuracy Score |

---

## 🧩 Dataset

**Dataset:** Breast Cancer Wisconsin (Diagnostic)  
**Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic)

- **Instances:** 569  
- **Features:** 30 numerical (radius, texture, area, compactness, etc.)  
- **Target:** Benign (0) / Malignant (1)

Data was clean, numerical, and required only scaling using `MaxAbsScaler`.  
Dimensionality was reduced to **5 principal components** using **PCA**, significantly improving training speed on the quantum simulator.

---

## 🧠 Model Implementation

### 🪐 Quantum SVM (QSVM)
- Implemented using **Qiskit Machine Learning**.
- Utilized **ZZFeatureMap** with 1 repetition and circular entanglement.
- Employed **FidelityQuantumKernel** and `ComputeUncompute` fidelity estimation.
- Model trained via `QSVC`.

### ⚙️ Classical SVM
- Implemented with `SVC` from scikit-learn using the `gamma='scale'` kernel.
- Served as a performance benchmark for the quantum model.

---

## 📊 Results

| Model | Accuracy |
|--------|-----------|
| Quantum SVM | **96.49%** |
| Classical SVM | **98.25%** |

Although the classical SVM slightly outperformed the QSVM, the project demonstrates that **quantum models already achieve comparable accuracy** on a moderate dataset using current simulators.

---

## 🔍 Key Findings

- Classical SVMs remain more efficient and slightly more accurate.  
- QSVMs are **computationally intensive**, mainly due to quantum kernel calculations.  
- PCA dramatically reduces training time without major accuracy loss.  
- Quantum machine learning shows promise but requires **hardware advancements** to realize full potential.

---

## 🚀 How to Run

```bash
# Clone repository
git clone https://github.com/<your-username>/quantum-vs-classical-svm.git
cd quantum-vs-classical-svm

# Create virtual environment (optional)
python -m venv .venv
source .venv/bin/activate  # or .venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Run notebook or script
jupyter notebook Quantum_vs_Classical_SVM.ipynb

