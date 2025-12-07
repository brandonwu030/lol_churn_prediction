# WinnieDaWu

# 🎮 League of Legends Player Churn Prediction

Predict whether players of League of Legends are likely to churn or stay active, using gameplay data and machine learning. Built using Python, Databricks, Random Forest classifier, and deployed with Streamlit.

---

## 📌 Problem Statement

Player churn is a major concern in the gaming industry. This project tackles churn prediction for *League of Legends*, one of the most played games globally. Using player data from the Korean server (Season 23), we aim to identify which players are at risk of leaving the game.

The goal is to help game developers proactively intervene to retain users and extend game lifecycle.

---

## 🧠 Machine Learning Approach

- **Task**: Supervised binary classification
- **Target Variable**: Player status → `Churn` vs `Active`
- **Model Used**: Random Forest Classifier (selected for superior performance)
- **Baseline Compared**: Logistic Regression
- **Frameworks**: Scikit-learn, Pandas, NumPy, MLflow

---

## 🗃️ Dataset

- **Source**: https://data.mendeley.com/datasets/74drmd922j/1
- **Features Include**:
  - Player Level
  - League Points
  - Average Score
  - Win %, Last 20 Match Win %
  - Losing Streak
  - Team performance metrics
  - Tier (Encoded)

---

## 🧪 Model Evaluation

| Metric       | Score     |
|--------------|-----------|
| Accuracy     | 0.7216917703755178   |
| Precision    | 0.8555879300957725   |
| Recall       | 0.7216917703755178   |
| F1 Score     | 0.7636824324096155   |
| Log loss     | 0.5484948530353664   |
| ROC AUC      | 0.7951665099697787   |

### 🔍 Visualizations:
- 📉 [Confusion Matrix](images/training_confusion_matrix.png) <img width="1050" height="700" alt="training_confusion_matrix" src="https://github.com/user-attachments/assets/b7ecf6d2-e8d4-42b9-a7c7-e0c838173dd7" />
- 🎯 [ROC Curve + AUC](images/training_roc_curve.png) ---<img width="1120" height="840" alt="training_roc_curve" src="https://github.com/user-attachments/assets/af47f43c-9e52-4ec3-97c0-7e573aa53501" />
- 📊 [Precision-Recall Curve](images/training_precision_recallcurve.png) <img width="1120" height="840" alt="training_precision_recall_curve" src="https://github.com/user-attachments/assets/c3191921-2a54-4e46-9bea-b79431d56f1e" />

---

## 🚀 Deployment

The model is deployed via a **Streamlit web app**, where users can input player statistics and receive a churn prediction.

### ▶️ Run the app locally:
```bash
# Install dependencies
pip install -r requirements.txt

# Run the Streamlit app in terminal 
streamlit run lol_churn_app.py


