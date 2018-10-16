# Problem:

This breast cancer database was obtained from Dr. Wolberg’s office at the University of Wisconsin Hospitals, Madison. Each record here contains values for different morphological and pathological features of a tumor dissected from any given patient. The class column indicates whether the patient has been characterized as the benign tumor or a malignant tumor.

Question 1:Build a classifier to identify patients with benign or malignant tumor based on the tumor characteristics

Question 2:As an oncologist, you would want to reduce your false positives as well as false negatives.

a. Identify the number of false positive and false negatives

b. Improve your classification model to reduce patients who are being predicted as having benign tumor but actually have malignant tumor.


# BreastCancerWisconsinDataSet
Analysis and Machine Learning Algorithms for https://archive.ics.uci.edu/ml/datasets/breast+cancer+wisconsin+(original) dataset.

# Data Preprocessing
The most important in this dataset is data preprocessing as "Bare Nuclei" column has ? Values which are replaced by 0.
Random Forest Classifier is used to view the feature importances.
Sample Code Number and Mitoses can be considered as not important.  
![alt text]()

# Algorithm
We can use Random Forest on the processed data.
First use Grid Search CV to find out the best parameters for the Random Forest Classifier.
After getting the best params we can run cross_val_score with cv=10 to get a score of around 96% .
Then using train_test_split we can try to find out the confusion matrix.
True Negatives 133 +- 2
False Positives 5 +- 2
True Positives 68 +-2
False Negatives 4 +-2

# More Analysis
As Tree algorithms have higher rate of false negatives as they cannot properly handle imbalanced datasets.
So we try to use Naïve Bayes Algorithm (Gaussian NB).
This improves our confusion matrix t
True Negatives 132 +- 2
False Positives 6 +- 2
True Positives 69 +- 1
False Negatives 2 +- 1

# Further Work
We can proceed to improve accuracy by using different algorithms Support Vector Machines with some improvement in feature selection.
More time devotion on this dataset may lead to an accuracy of 98% with very less number of false negatives.
