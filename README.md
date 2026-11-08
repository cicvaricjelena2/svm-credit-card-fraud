Credit Card Fraud Detection Using Machine Learning

Project Overview

Credit card fraud detection is a binary classification problem that aims to identify fraudulent transactions while minimizing the number of legitimate transactions incorrectly flagged as fraud.

This project explores and compares several machine learning algorithms for detecting fraudulent credit card transactions using a highly imbalanced dataset.

The main objective is to investigate how different classification approaches perform when dealing with rare events and to evaluate the impact of class imbalance handling on fraud detection performance.

Dataset

Dataset: Credit Card Fraud Detection – Kaggle

The dataset contains anonymized credit card transactions made by European cardholders.

Features include:

* V1–V28: Numerical features obtained through PCA transformation.
* Amount: Transaction amount.
* Class: Target variable (0 = legitimate transaction, 1 = fraudulent transaction).

The Time feature was excluded from the analysis.

One of the main challenges is the severe class imbalance, as fraudulent transactions represent only a very small proportion of all transactions.

Methodology

The project follows a machine learning pipeline consisting of data preprocessing, model training, classification, and performance evaluation.

1. Data Preprocessing

* Loading and exploring the dataset using Pandas.
* Analyzing the distribution of legitimate and fraudulent transactions.
* Separating features and target variables.
* Splitting the dataset into training and testing subsets using stratified sampling.
* Standardizing features using StandardScaler.

2. Exploratory Data Analysis

The dataset is explored to understand the distribution of transaction classes and the challenges associated with imbalanced classification.

Principal Component Analysis (PCA) is also applied to visualize the transactions in a two-dimensional feature space.

3. Machine Learning Models

Five classification approaches are investigated:

Linear Support Vector Machine (SVM)

A linear SVM classifier is trained using class-weight balancing to account for the imbalance between legitimate and fraudulent transactions.

RBF Support Vector Machine (SVM)

An SVM with a Radial Basis Function kernel is implemented to capture nonlinear decision boundaries. Due to computational complexity, a stratified subset of the training data is used.

SVM with SMOTE

The Synthetic Minority Over-sampling Technique (SMOTE) is applied to the training data to generate synthetic fraudulent transactions and balance the class distribution.

A linear SVM classifier is subsequently trained on the resampled dataset.

Gaussian Naive Bayes

A probabilistic classifier based on Bayes’ theorem is implemented. Different cost ratios and decision thresholds are explored to investigate the trade-off between precision and recall.

K-Nearest Neighbors (KNN)

A distance-weighted KNN classifier is implemented. Different values of the number of neighbors (k) are investigated and compared.

4. Model Evaluation

The performance of the classifiers is evaluated using several metrics:

* Precision
* Recall
* F1-score
* ROC-AUC
* Confusion Matrix

ROC curves are generated to compare the classification performance of the implemented models.

Special attention is given to recall and F1-score for the fraudulent class, since detecting fraudulent transactions is the primary objective of the project.

Technologies & Libraries

* Python
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* Imbalanced-learn
* Jupyter Notebook

Repository Structure

credit-card-fraud-detection/
│
├── README.md
├── fraud_detection_analysis.ipynb
├── dataset_creditcards.csv
└── .gitignore

The dataset is not included in the repository and must be downloaded separately.

How to Run

1. Clone the repository:

git clone https://github.com/cicvaricjelena2/svm-credit-card-fraud.git

2. Navigate to the project directory:

cd svm-credit-card-fraud

3. Install the required libraries:

pip install numpy pandas matplotlib scikit-learn imbalanced-learn jupyter

4. Download the dataset from Kaggle and place dataset_creditcards.csv in the project directory.
5. Launch Jupyter Notebook:

jupyter notebook

6. Open the notebook and execute the cells.

Key Takeaways

This project demonstrates the implementation and comparison of multiple machine learning approaches for an imbalanced binary classification problem.

It explores the importance of preprocessing, class imbalance handling, probabilistic classification, decision thresholds, and evaluation metrics when developing fraud detection systems.

The experiments highlight why accuracy alone is insufficient for evaluating classifiers in applications where the minority class is of particular interest.

Author

Jelena Cicvarić

Electrical Engineering | Machine Learning | Data Science

GitHub Profile
