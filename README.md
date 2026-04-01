# SecurePay FinTech – Fraud Detection using Unsupervised Learning

## 📌 Project Overview
Financial fraud is a rare but critical problem in FinTech systems. Traditional supervised models fail due to extreme class imbalance.

This project builds an **Unsupervised Anomaly Detection System** to detect fraudulent transactions by learning normal transaction behaviour.

---

## 🎯 Objective
Detect anomalous transactions using:
- Isolation Forest
- Local Outlier Factor (LOF)

Instead of predicting fraud directly, the model identifies transactions that deviate from normal patterns.

---

## 📂 Dataset
Credit Card Fraud Detection Dataset (Kaggle)

Features:
- PCA-transformed: V1 to V28
- Time
- Amount
- Class (0 = Normal, 1 = Fraud)

---

## ⚙️ Data Preprocessing
- Handled extreme imbalance
- Applied **RobustScaler** to:
  - Amount
  - Time
- Retained PCA features as-is

---

## 🤖 Models Used

### 1. Isolation Forest
Tree-based anomaly detection  
Isolates rare and different data points quickly

### 2. Local Outlier Factor (LOF)
Density-based anomaly detection  
Detects low-density outliers

---

## 📊 Evaluation Metrics
Accuracy is misleading for fraud detection.

Used:
- Precision
- Recall
- F1 Score
- Confusion Matrix
- Precision–Recall Curve

---

## 📉 Visualization
- Class imbalance plot
- PCA 2D visualization
- Detected anomaly scatter plots

---

## 🧠 Final Recommendation
Isolation Forest performed better in balancing fraud detection and false positives.

Recommended configuration:

Isolation Forest  
Contamination = 0.001  

This allows detection of rare fraud cases while maintaining a manageable false alarm rate.

---

## 🛠️ Tech Stack
- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

---

## ▶️ How to Run

1. Create environment:
conda create -n securepay python=3.10

2. Activate:
conda activate securepay

3. Install dependencies:
pip install pandas numpy matplotlib seaborn scikit-learn jupyter

4. Run notebook:
Open notebooks/SecurePay_Fraud_Detection.ipynb

---

## 📌 Project Outcome
Built an unsupervised fraud detection pipeline capable of identifying anomalous financial transactions using density-based and tree-based approaches.