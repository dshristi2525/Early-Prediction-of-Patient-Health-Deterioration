# Early-Prediction-of-Patient-Health-Deterioration
# 🩺 Patient Health Deterioration Prediction using LSTM

## 📌 Project Overview
This project implements a **Deep Learning–based clinical risk prediction system** to identify **early patient deterioration** using **time-series vital signs data**.  
An **LSTM (Long Short-Term Memory) neural network** is trained on sequential health data to predict whether a patient is likely to deteriorate, enabling early medical intervention.

The system also includes **risk-level classification**, **trend analysis**, and **clinical interpretability**, making it suitable as a medical decision-support prototype.
---
## 🎯 Problem Statement
Continuous monitoring of patient vitals is critical in healthcare.  
Manual interpretation of multi-day health trends is:
- Time-consuming  
- Error-prone  
- Difficult to scale  

This project explores how **LSTM-based sequence models** can automatically detect **early warning signs of patient deterioration**.
---
## 📊 Data Description
- **Data Type:** Synthetic medical time-series data  
- **Patients:** 500  
- **Days per Patient:** 14  
- **Features Used:**
  - Temperature (°C)
  - SpO₂ (%)
  - Heart Rate (bpm)
- **Target Label:** Patient Deterioration (Binary)

Synthetic data is generated to simulate **realistic recovery and deterioration patterns**.
---
## ⚙️ Technologies Used
- Python  
- NumPy, Pandas  
- Matplotlib  
- Scikit-learn  
- TensorFlow / Keras  
- LSTM (Deep Learning)
  
  ## 🧠 Model Architecture
- **Optimizer:** Adam  
- **Loss Function:** Binary Crossentropy  
- **Task:** Binary Classification  
---
## 🏋️ Training Details
- Sequence Length: **5 days**  
- Train/Test Split: **80/20 (stratified)**  
- Validation Split: **20% of training data**  
- Epochs: **20**  
- Batch Size: **32**  
---
## 📈 Model Evaluation Metrics
The model is evaluated using **clinically relevant classification metrics**:

| Metric | Value |
|------|-------|
| **Accuracy** | **0.8078** |
| **Precision** | **0.9007** |
| **Recall (Sensitivity)** | **0.4441** |
| **F1 Score** | **0.5948** |
| **Specificity** | **0.9772** |
| **ROC-AUC Score** | **0.8198** |
---
## 🧮 Confusion Matrix
The confusion matrix is computed to analyze:
- True Positives (TP)
- True Negatives (TN)
- False Positives (FP)
- False Negatives (FN)

This helps assess the model’s behavior in **clinical decision-making scenarios**, where false negatives are critical.
---
## 🟢🟡🔴 Risk Level Classification
Predicted probabilities are mapped to **clinical risk levels**:

- **GREEN (< 0.3)** → Stable  
- **YELLOW (0.3 – 0.6)** → Monitor Closely  
- **RED (> 0.6)** → Doctor Attention Required  
---
## 📊 Trend Analysis & Explainability
For individual patients, the system:
- Plots last 5-day health trends
- Analyzes direction of:
  - Temperature
  - SpO₂
  - Heart Rate
- Provides **rule-based clinical interpretation** to identify:
  - Normal recovery patterns
  - Abnormal deterioration patterns
