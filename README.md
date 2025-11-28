# 🚀 Bank Churn Prediction using MLflow & Flask

A complete end-to-end **Machine Learning** system designed to predict whether a bank customer is likely to churn. This project demonstrates full lifecycle ML — including **data processing**, **model training**, **experiment tracking**, and **web deployment**.

---

## 📌 Table of Contents
- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Technologies Used](#technologies-used)
- [Installation & Setup](#installation--setup)
- [Running the Application](#running-the-application)
- [API Usage](#api-usage)
- [Model Performance](#model-performance)
- [Project Structure](#project-structure)
- [Future Improvements](#future-improvements)

---

## 🔍 Project Overview
This system predicts whether a bank customer will **churn** based on features such as:

- Age  
- Credit Score  
- Geography & Gender  
- Tenure  
- Balance & Estimated Salary  
- Number of Products  
- Has Credit Card  
- Active Member Status  

The dataset is **imbalanced**, and **SMOTE** is used to oversample minority churn cases for better model generalization.

Multiple ML models were evaluated — the **Gradient Boosting Classifier** achieved the best performance and is used in deployment.  
Model tracking and versioning are handled through **MLflow**.

---

## ✨ Key Features

✔ End-to-end ML pipeline  
✔ Data validation, transformation, and feature scaling  
✔ Imbalanced data handling with SMOTE  
✔ Experiment tracking using MLflow  
✔ Flask API for real-time predictions  
✔ Clean, modular folder structure for scalability  

---

## 🧰 Technologies Used

| Category | Tools |
|---------|-------|
| Machine Learning | Scikit-learn, Pandas, NumPy |
| Deployment | Flask |
| Experiment Tracking | MLflow |
| Data Processing | SMOTE, One-Hot Encoding |
| Environment Management | Conda |

---

## ⚙️ Installation & Setup

# Clone the repository
git clone <repo-url>
cd bank-churn-prediction

# Create conda environment
conda create -n churn python=3.10 -y
conda activate churn

# Install dependencies
pip install -r requirements.txt

## ▶️ Running the Application
python app.py

# The server will start on:
➡️ http://127.0.0.1:5000/

# 🌐 API Usage
🏠 Default Route
GET http://127.0.0.1:5000/
Returns a welcome message.

# 📈 Prediction Route
POST http://127.0.0.1:5000/predict

# Example Input (JSON)
{
  "CreditScore": 650,
  "Geography": "France",
  "Gender": "Male",
  "Age": 40,
  "Tenure": 5,
  "Balance": 100000,
  "NumOfProducts": 2,
  "HasCrCard": 1,
  "IsActiveMember": 1,
  "EstimatedSalary": 50000
}

# Example Output
{
  "Churn Prediction": "Will Not Churn"
}

## 📊 Model Performance
Metric	Score
Accuracy	86%
Precision	66%
Recall	62%
F1-Score	60%

👉 Best Model: Gradient Boosting Classifier
📌 Metrics & model artifacts tracked using MLflow

## 📁 Project Structure

```text
.
├── app.py
├── requirements.txt
├── README.md
├── artifacts/            # Saved ML model and preprocessing objects
├── mlruns/               # MLflow experiment tracking
└── src/
    ├── components/       # Data ingestion, validation, training modules
    ├── pipelines/        # Training and prediction pipelines
    ├── utils/            # Helper utilities
    └── logger/           # Logging system

```
---
## 🚀 Future Improvements

🔹 Add frontend UI for prediction
🔹 Deploy using Docker & Cloud (AWS/Azure/Render)
🔹 Add advanced hyperparameter tuning
🔹 Plot analytics dashboard for model insights
🔹 Add ROC-AUC and confusion matrix visualization
---
