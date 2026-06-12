# predictive-maintenance-ml
Predicting machine failures using industrial sensor data with Logistic Regression and Random Forest models.
# Machine Learning-Based Predictive Maintenance System

## Overview

This project uses machine learning techniques to predict machine failures using industrial sensor data. The objective is to identify potential equipment failures before they occur by analyzing operational parameters such as temperature, rotational speed, torque, and tool wear.

The project was developed using the AI4I 2020 Predictive Maintenance Dataset and demonstrates the application of machine learning to a real-world engineering problem.

---

## Problem Statement

Unexpected machine failures can result in production downtime, increased maintenance costs, and operational inefficiencies. The goal of this project is to build a classification model that can predict machine failures using sensor measurements collected during machine operation.

---

## Dataset

**Dataset:** AI4I 2020 Predictive Maintenance Dataset

### Features

* Machine Type (L, M, H)
* Air Temperature [K]
* Process Temperature [K]
* Rotational Speed [rpm]
* Torque [Nm]
* Tool Wear [min]

### Target Variable

* **0** → No Machine Failure
* **1** → Machine Failure

### Dataset Statistics

* Total Samples: 10,000
* Failure Cases: 339
* Non-Failure Cases: 9,661
* Failure Rate: 3.39%

The dataset is highly imbalanced, making Recall and F1-Score important evaluation metrics.

---

## Methodology

### Data Preprocessing

* Removed identifier columns (UDI, Product ID)
* Removed failure-type columns (TWF, HDF, PWF, OSF, RNF)
* Applied one-hot encoding to machine type
* Split dataset into training and testing sets

### Exploratory Data Analysis

Performed:

* Class distribution analysis
* Feature inspection
* Failure frequency analysis
* Correlation analysis

### Models Used

#### Logistic Regression

Used as a baseline classification model with feature scaling and class balancing.

#### Random Forest Classifier

Used as the primary model for machine failure prediction and feature importance analysis.

---

## Results

### Logistic Regression

| Metric    | Value |
| --------- | ----- |
| Accuracy  | 82%   |
| Precision | 14%   |
| Recall    | 82%   |
| F1-Score  | 24%   |

### Random Forest

| Metric    | Value |
| --------- | ----- |
| Accuracy  | 95%   |
| Precision | 42%   |
| Recall    | 82%   |
| F1-Score  | 55%   |

### Key Observation

The Random Forest model achieved the best overall performance by significantly improving precision and F1-score while maintaining high recall. This indicates that the model was able to detect machine failures while reducing false alarms.

---

## Feature Importance Analysis

Random Forest feature importance was used to identify which operational parameters contributed most to machine failure prediction. This helps in understanding which machine conditions have the strongest influence on equipment health.

---

## Skills Applied

* Data Preprocessing
* Exploratory Data Analysis (EDA)
* One-Hot Encoding
* Classification Models
* Logistic Regression
* Random Forest
* Model Evaluation
* Confusion Matrix Analysis
* Precision, Recall, and F1-Score
* Feature Importance Analysis

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Jupyter Notebook / Kaggle Notebook

---

## Future Improvements

* Hyperparameter tuning
* XGBoost implementation
* Real-time sensor integration
* Streamlit deployment
* IoT-based predictive maintenance system
* Embedded sensor data acquisition using microcontrollers

---

## Project Structure

```text
predictive-maintenance-ml/
│
├── predictive_maintenance.ipynb
├── README.md
├── requirements.txt
└── images/
```

---

## Conclusion

This project demonstrates how machine learning can be applied to predictive maintenance using industrial sensor data. By comparing Logistic Regression and Random Forest models, the project highlights the importance of model evaluation beyond accuracy and showcases the practical use of ML techniques in engineering applications.


