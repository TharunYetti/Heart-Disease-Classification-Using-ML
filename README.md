# Heart-Disease-Classification-Using-ML

This project implements a machine learning pipeline for predicting the likelihood of heart disease in patients based on various clinical parameters. The system uses multiple classification models and combines their predictions using a majority voting mechanism to provide a final decision.

---

## Project Overview
The system:
- Accepts user inputs as a dataframe with patient clinical data.
- Preprocesses the input using pipelines saved with `pickle`.
- Uses three trained machine learning models (K-Nearest Neighbors, Decision Tree, and Support Vector Classifier) to make predictions.
- Combines predictions from all models to provide a final majority vote classification.

---

## Features
1. **Multiple Models**:
   - K-Nearest Neighbors (KNN)
   - Decision Tree (DT)
   - Support Vector Classifier (SVC)
2. **Preprocessing**:
   - Handles categorical and numerical data preprocessing.
   - Saves preprocessing pipelines for reuse.
3. **Majority Voting**:
   - Aggregates predictions from all models to provide a robust final output.
4. **Scalable Input**:
   - Accepts multiple rows of data in a single input.

---

## Setup Instructions

### Prerequisites
1. Python 3.7+
2. Libraries:
   - pandas
   - numpy
   - scikit-learn
   - pickle (built-in library)

### Clone the Repository
```bash
git clone <repository_url>
cd Heart-Disease-Classification-Using-ML
```

### Files and Pipelines
- `knn_pipeline.pkl`: Preprocessing and model pipeline for KNN.
- `svc_pipeline.pkl`: Preprocessing and model pipeline for SVC.
- `dt_pipeline.pkl`: Preprocessing and model pipeline for Decision Tree.

---

## Usage Instructions

### 1. Input Data Format
The input data should be provided as a pandas DataFrame with the following columns:
```plaintext
['age', 'sex', 'cp', 'trestbps', 'chol', 'fbs', 'restecg', 'thalach', 'exang', 'oldpeak', 'slope', 'ca', 'thal']
```
1. age
2. sex : 0 = female; 1 = male
3. chest pain type : 0 = No Pain; 1 = Low; 2 = Medium; 3 = High
4. resting blood pressure
5. serum cholestoral in mg/dl
6. fasting blood sugar : 0 if <= 120 mg/dl; 1 if >120 mg/dl
7. resting electrocardiographic results (values 0,1,2)
8. maximum heart rate achieved
9. exercise induced angina
10. oldpeak = ST depression induced by exercise relative to rest
11. the slope of the peak exercise ST segment
12. number of major vessels (0-3) colored by flourosopy
13. thal: 0 = normal; 1 = fixed defect; 2 = reversable defect

### 2. Output
The output will be a DataFrame with:
- Final majority vote classification.

---

## Contribution
Feel free to contribute by raising issues or submitting pull requests. Ensure to follow the standard contribution guidelines.

