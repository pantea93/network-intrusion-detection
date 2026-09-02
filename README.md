# network-intrusion-detection
Machine learning network intrusion detection using the NSL-KDD dataset.
# Network Intrusion Detection using Machine Learning

An end-to-end machine learning project for detecting anomalous network
traffic using the NSL-KDD dataset.

## Project Overview

This project develops a binary classification pipeline to classify network
connections as either **Normal** or **Anomalous**.

Four machine learning classifiers are evaluated:

- L1-Regularised Logistic Regression
- Linear Discriminant Analysis (LDA)
- k-Nearest Neighbours (kNN)
- Random Forest

Each classifier is evaluated both **with and without Principal Component
Analysis (PCA)**.

## Machine Learning Pipeline

The project includes:

- Data loading and cleaning
- Exploratory Data Analysis (EDA)
- Stratified training and validation split
- One-hot encoding of categorical features
- Feature scaling
- Feature selection using Random Forest feature importance
- Principal Component Analysis (PCA)
- Model selection and evaluation
- Final evaluation on the untouched NSL-KDD test set

## PCA

Feature selection reduced the encoded feature space to the 90 highest-ranked
features.

PCA further reduced these 90 features to **61 principal components** while
retaining approximately **95% of the cumulative explained variance**.

## Final Results

Random Forest achieved the strongest overall performance.

- **Random Forest with PCA** achieved the highest accuracy (79.54%), recall
  (66.54%), and F1-score (78.73%).
- **Random Forest without PCA** achieved the highest precision (96.83%),
  specificity (97.29%), and ROC-AUC (96.03%).

The results show that the effect of PCA depends on the classifier. PCA
improved all reported metrics for kNN and improved accuracy, recall and
F1-score for Random Forest, while its effect on the linear classifiers
was more mixed.

## Repository Contents

- `Network_Intrusion_Detection.ipynb` — complete machine learning analysis
- `figures/` — visualisations generated during the analysis
- `final_model_results.csv` — final model performance
- `pca_impact_results.csv` — comparison of performance with and without PCA

## Dataset

This project uses the **NSL-KDD network intrusion detection dataset**.

The original training and test datasets are not included in this repository.
