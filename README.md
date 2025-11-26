# Diabetes Prediction Model

This project builds a machine learning model to predict whether a person has diabetes based on their lifestyle, medical conditions, and demographic information. The dataset used in this project contains over **250,000 records** collected from a real-world U.S. health survey. The goal of the project is to create a model that can help identify people who may be at high risk of diabetes.

---

## 📂 Project Structure

/dataset
└── diabetes_dataset.csv # Dataset used for training and evaluation

/model
└── diabetes_model.joblib # Saved XGBoost model for future predictions

diabetes_prediction.ipynb # Jupyter Notebook containing model training, EDA, and evaluation

---

## 📘 Project Overview

1. **Data Understanding & Cleaning**  
   - Loaded and analyzed all features such as BMI, age, blood pressure, cholesterol, smoking habits, and physical activity.  
   - Handled outliers (especially in BMI) using clipping to keep extreme but meaningful health values.

2. **Imbalance Handling**  
   - The dataset is imbalanced (approx 86% non-diabetic, 14% diabetic).  
   - Used `scale_pos_weight` in XGBoost to give more importance to diabetic cases.

3. **Model Training**  
   - Trained Decision Tree, Random Forest, and XGBoost models.  
   - Selected **XGBoost** as the final model because it gave stable performance and handled imbalance well.

4. **Improving Recall (Medical Priority)**  
   - Lowered the prediction threshold from 0.5 to 0.35 to catch more diabetic cases.  
   - Achieved **high recall**, which is important for medical screening.

5. **Model Saving**  
   - The best model is saved as `diabetes_model.joblib` inside the `/model` folder.

---

## 🚀 How to Use  
Open the notebook `diabetes_prediction.ipynb` to view the complete workflow:  
- Exploratory Data Analysis  
- Model building  
- Evaluation  
- Feature importance  
- Final model saving

You can load the trained model from the `/model` folder for making new predictions.

---
