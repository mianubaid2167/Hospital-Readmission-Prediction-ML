# 🏥 Hospital Readmission Prediction using Machine Learning

## 📌 Project Overview

This project focuses on predicting whether a diabetic patient will be readmitted to the hospital after discharge. The dataset was cleaned, explored, and preprocessed before applying multiple machine learning algorithms to classify patient readmission outcomes.

The project also demonstrates feature engineering, preprocessing pipelines, class imbalance handling using SMOTE, model comparison, clustering, feature importance analysis, and fairness evaluation.

---

## 🎯 Objectives

- Clean and preprocess the hospital readmission dataset.
- Perform Exploratory Data Analysis (EDA).
- Engineer new meaningful features.
- Build reusable preprocessing pipelines.
- Handle class imbalance using SMOTE.
- Train and compare multiple machine learning models.
- Analyze important features affecting hospital readmission.
- Evaluate model fairness across demographic groups.
- Perform patient risk segmentation using K-Means clustering.

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- SQLite3
- Scikit-learn
- Imbalanced-learn (SMOTE)
- Jupyter Notebook

---

## 📂 Project Structure

```
Hospital_Readmission_Project/
│
├── data/
│   └── diabetic_data.csv
│
├── notebooks/
│   ├── 01_Data_Loading.ipynb
│   ├── 02_Data_Cleaning.ipynb
│   ├── 03_EDA.ipynb
│   ├── 04_Feature_Engineering.ipynb
│   ├── 05_Preprocessing_and_Pipeline.ipynb
│   ├── 06_Logistic_Regression.ipynb
│   ├── 07_Decision_Tree.ipynb
│   ├── 08_SMOTE.ipynb
│   ├── 09_KNN.ipynb
│   ├── 10_KMeans_Clustering.ipynb
│   ├── 11_Feature_Importance.ipynb
│   ├── 12_Fairness_Analysis.ipynb
│   └── 13_Final_Comparison.ipynb
│
├── README.md
└── requirements.txt
```

---

## 📊 Dataset Information

The dataset contains hospital records of diabetic patients and predicts the **readmitted** status:

- **NO** → No readmission
- **>30** → Readmitted after 30 days
- **<30** → Readmitted within 30 days

---

## 🧹 Data Preprocessing

The following preprocessing steps were performed:

- Loaded the dataset
- Removed duplicate records
- Handled missing values
- Selected relevant features
- Feature Engineering
- Train-Test Split
- StandardScaler
- OneHotEncoder
- ColumnTransformer
- Pipeline

---

## ⚙ Feature Engineering

Two new features were created:

- **total_prior_visits**
  - Sum of inpatient, outpatient, and emergency visits.

- **had_previous_visit**
  - Binary feature indicating whether the patient had previous hospital visits.

These engineered features improved the model's ability to learn patient history.

---

## 📈 Exploratory Data Analysis (EDA)

The following visualizations were performed:

- Class Distribution
- Correlation Heatmap
- Histograms
- Count Plots
- Scatter Plots
- Box Plots

---

## 🤖 Machine Learning Models

The following classification algorithms were implemented:

- ✅ Logistic Regression
- ✅ Logistic Regression with SMOTE
- ✅ Decision Tree Classifier
- ✅ K-Nearest Neighbors (KNN)

---

## ⚖ Handling Class Imbalance

Since the dataset was highly imbalanced, SMOTE (Synthetic Minority Oversampling Technique) was applied.

SMOTE generated synthetic samples for the minority class (<30), improving recall for high-risk patients.

The project compares:

- Logistic Regression (Balanced)
- Logistic Regression (SMOTE)

---

## 📊 Model Evaluation

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Classification Report

Special attention was given to Recall for the `<30` class because correctly identifying high-risk patients is important in healthcare applications.

---

## 🌳 Feature Importance

Decision Tree feature importance analysis identified the most influential features affecting hospital readmission.

Some of the most important features include:

- discharge_disposition_id
- total_prior_visits
- number_inpatient
- number_diagnoses
- payer_code
- time_in_hospital

This analysis helped explain how the model makes predictions.

---

## 👥 Fairness Analysis

The trained model was evaluated across different demographic groups.

Fairness was analyzed using:

- Gender-wise performance
- Age-group performance

Performance differences between groups were examined to identify potential prediction bias.

---

## 📌 K-Means Clustering

Unsupervised learning was also performed using K-Means clustering.

The Elbow Method was used to determine the optimal number of clusters.

Patient groups were segmented to identify different readmission risk profiles.

---

## 📈 Model Comparison

The following models were compared:

| Model | Accuracy | Notes |
|---------|-----------|------------------------------|
| Logistic Regression | ✔ | Baseline model |
| Logistic Regression + SMOTE | ✔ | Improved minority recall |
| Decision Tree | ✔ | Interpretable model |
| K-Nearest Neighbors | ✔ | Distance-based classifier |

---

## 🚀 Future Improvements

- Hyperparameter Tuning using GridSearchCV
- Random Forest Classifier
- XGBoost Classifier
- Cross Validation
- Model Deployment using Flask or Streamlit
- Save trained models using Joblib
- Build a hospital readmission prediction web application

---

## 👨‍💻 Author

**Muhammad Ubaid Ul Hassan**

Software Engineering Student

Machine Learning | Data Science | Python Developer

Currently learning practical Machine Learning by building real-world healthcare prediction projects.