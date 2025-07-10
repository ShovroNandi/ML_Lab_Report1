
# 🧪 Diabetes Prediction using Linear Regression

This project demonstrates how to use **Linear Regression** to predict diabetes using patient medical data. It is implemented using Python and scikit-learn on the famous Diabetes Dataset.

---

## 📂 Dataset Source

This project uses the [Diabetes Dataset](https://www.kaggle.com/datasets/saurabh00007/diabetescsv) from Kaggle.

You can download the CSV file directly from the above link.



## 📂 Dataset Description

The dataset contains **768 samples** and **9 attributes**:

| Feature | Description |
|---------|-------------|
| Pregnancies | Number of pregnancies |
| Glucose | Plasma glucose concentration |
| BloodPressure | Diastolic blood pressure (mm Hg) |
| SkinThickness | Triceps skinfold thickness (mm) |
| Insulin | 2-Hour serum insulin (mu U/ml) |
| BMI | Body mass index (weight in kg/(height in m)^2) |
| DiabetesPedigreeFunction | Diabetes pedigree function |
| Age | Age of the patient (in years) |
| Outcome | Class variable (0 or 1) |

---

## ⚙️ Preprocessing Steps

1. Replaced **0 values** in key columns (`Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, `BMI`) with the **median** of the respective columns.
2. Replaced the **first row’s Glucose** value with the **maximum** value from the Glucose column.
3. Replaced Glucose values with the **minimum** value for patients having the **lowest age** in the dataset.

---

## 🧠 Model: Linear Regression

Although Linear Regression is typically used for continuous prediction, it is adapted here for binary classification by **rounding the output** to 0 or 1.

### 📌 Mathematical Formula:

\[y^=w1x1 + w2x2 +⋯+ wnxn +b\]

Where:
- \(y^): predicted outcome
- \(x1, x2, ..., xn\): input features
- \(w1, w2, ..., wn\): weights (coefficients)
- \(b\): bias (intercept)

---

## 📊 Evaluation Metrics

After rounding predictions to 0 or 1, the following classification metrics are used:

## ✅ Confusion Matrix

A confusion matrix is a table used to evaluate the performance of a classification model by comparing actual and predicted labels:

|               | Predicted 0 | Predicted 1 |
|---------------|-------------|-------------|
| **Actual 0**  | TN          | FP          |
| **Actual 1**  | FN          | TP          |

- **TP (True Positive):** The model correctly predicted the patient has diabetes.
- **TN (True Negative):** The model correctly predicted the patient does not have diabetes.
- **FP (False Positive):** The model incorrectly predicted the patient has diabetes (but actually doesn’t).
- **FN (False Negative):** The model incorrectly predicted the patient does not have diabetes (but actually does).


### ✅ Accuracy
Accuracy measures how often the model is correct.

**Formula:**

Accuracy = (TP + TN) / (TP + TN + FP + FN)

### ✅ Precision
Precision measures how many of the positive predictions made by the model were actually correct.

**Formula:**

Precision = TP / (TP + FP)

### ✅ Recall 
Recall measures how many of the actual positive cases were correctly identified by the model.

**Formula:**

Recall = TP / (TP + FN)

### ✅ F1-Score
F1-score is the harmonic mean of Precision and Recall. It provides a balance between both.

**Formula:**

F1-Score = 2×(Precision×Recall) / (Precision+Recall)

---

## 📈 Results

| Metric | Value |
|--------|--------|
| Accuracy | 81.16% |
| Precision | 73.68% |
| Recall | 59.57% |
| F1-Score | 65.88% |

Confusion Matrix:\
[[97 10]\
[19 28]]

## 🚀 How to Run
1. Clone the repo
2. Install requirements
3. Run the Python script

### Technologies:
- Python
- Numpy
- Matplotlib
- Pandas
- scikit-learn

