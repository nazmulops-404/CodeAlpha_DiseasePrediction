# Disease Prediction (Breast Cancer)

CodeAlpha Machine Learning Internship, Task 4.

## Objective
Predict whether a tumor is malignant (cancer) or benign (not cancer) from patient measurements.

## Dataset
Breast Cancer Wisconsin dataset, loaded from Scikit-learn.
* 569 patients, 30 numeric features (radius, texture, area, concavity and others)
* No missing values
* Target: 0 = malignant (212 cases), 1 = benign (357 cases)

## Method
1. Loaded the data and checked for missing values.
2. Split into 80% training and 20% testing (stratified, random_state=42).
3. Scaled features with StandardScaler. The scaler was fitted on training data only.
4. Trained four models: Logistic Regression, SVM, Random Forest, XGBoost.
5. Evaluated with Accuracy, Precision, Recall, F1 Score and Confusion Matrix.

## Results

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---|---|---|---|
| Logistic Regression | 98.25% | 98.61% | 98.61% | 98.61% |
| SVM | 98.25% | 98.61% | 98.61% | 98.61% |
| Random Forest | 95.61% | 95.89% | 97.22% | 96.55% |
| XGBoost | 95.61% | 94.67% | 98.61% | 96.60% |

## Conclusion
Logistic Regression gave the best overall result, tied with SVM. It is also the simplest model, which makes it easier to explain and trust.

In medical prediction, Recall matters most. Missing a sick patient costs more than a false alarm. All four models reached a Recall between 97% and 99%.

## Limitations
* The test set has only 114 patients, so small differences between models are not strong evidence.
* The data comes from one source. The model is a learning project and not a medical tool.

## How to run
1. Open the notebook file in Google Colab.
2. Click Runtime, then Run all.

## Tools
Python, Pandas, Scikit-learn, XGBoost, Matplotlib
