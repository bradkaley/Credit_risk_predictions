# Credit_risk_predictions
The notebooks in this repository model credit risks for loans using machine learning. The loan data is imbalanced so the models have to be evaluated with imbalanced classes. The first notebook uses resampling models and the second uses ensemble learning.

---

## Resampling

Based on the modeling, conclusions were drawn to answer the following questions:

### 1. Which model had the best balanced accuracy score?

The random oversampling and SMOTE oversampling models tied for the best score (0.9934649587814939).

### 2. Which model had the best recall score?

Every model tied with a 99% (0.99) recall score.

### 3. Which model had the best geometric mean score?

All models except for the simple logistic regression model tied with a 99% (0.99) geometric mean score.

Overall, all the models were very similar and accurate. If I were to be pick one model to use moving forward for this dataset, I would select the naive random oversampling model. The reason for not selecting the cluster centroid model is because this model removes data points and replaces them with synthetic points, and typically I would not want to lose valuable data. Additionally, the naive random oversampling model only duplicates existing data points, unlike SMOTE which creates new synthetic data points; therefore, the naive random oversampling model is preferable over SMOTE.

---

## Ensemble Learning

Since the Easy Ensemble attribute "n_features_in_" was deprecated and thus Easy Ensember Classifier cannot be run, the Balanced Random Forest Classifier is compared to the Random Undersampler Model. Based on the modeling, conclusions were drawn to answer the following questions:

### 1. Which model had the best balanced accuracy score?

The random undersampling model had the better balance accuracy score (0.8221309473089498 compared to 0.7561059192916486).

### 2. Which model had the best recall score?

The balanced random forest classifier had the better recall score (0.86 compared to 0.80).

### 3. Which model had the best geometric mean score?

The random undersampling model had the better geometric score (0.82 compared to 0.75).

### 4. What are the top three features?

The top three features are total received principal (total_rec_prncp), total payment (total_pymnt), and total payment invoiced (total_pymnt_inv).