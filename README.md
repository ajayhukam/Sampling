# Sampling

Project Overview
The script uses the following models to predict credit card fraud:

Logistic Regression (M1)
Random Forest Classifier (M2)
Support Vector Classifier (Linear Kernel) (M3)
Support Vector Classifier (RBF Kernel) (M4)
Random Forest Classifier (with 200 estimators) (M5)
The class imbalance issue in the dataset is addressed using two sampling techniques:

SMOTE (Synthetic Minority Over-sampling Technique)
Random Under-Sampling
Data Source
The dataset used in this project is the Creditcard_data.csv file, which contains credit card transaction data. Each transaction is labeled as either fraudulent or non-fraudulent (Class: 1 for fraudulent, 0 for non-fraudulent).

Requirements
You need to have the following Python packages installed to run the script:

pandas
numpy
scikit-learn
imbalanced-learn
You can install these dependencies using pip:

Copy
pip install pandas numpy scikit-learn imbalanced-learn
How to Run the Code
Download the dataset: Make sure you have the Creditcard_data.csv file available. The script expects the file to be located at /content/Creditcard_data.csv. You can modify the path as needed.

Script Execution: Run the Python script provided. The script will:

Load the dataset and preprocess it.
Apply the balancing techniques (SMOTE or Random Under-Sampling).
Train the specified models using 5 different sample sizes.
Evaluate the models using accuracy on the test set.
The results of the model evaluation (accuracy scores for each model and technique) will be printed.

Sampling Techniques
The script uses 5 sample sizes (ranging from 10% to 50% of the balanced dataset) for each balancing technique. The following sampling sizes are used:

Sampling1: 10% of the balanced dataset
Sampling2: 20% of the balanced dataset
Sampling3: 30% of the balanced dataset
Sampling4: 40% of the balanced dataset
Sampling5: 50% of the balanced dataset
Results
After training and evaluation, the accuracy of each model under each sampling technique is printed in a DataFrame. The best performing model (highest accuracy) is highlighted for further analysis.

Example Output
After running the script, you will see an output similar to this:

java
Copy
Accuracy Results:
                     Sampling1  Sampling2  Sampling3  Sampling4  Sampling5
M1 (LogisticRegression)      0.90       0.91       0.92       0.89       0.90
M2 (RandomForest)           0.92       0.93       0.94       0.91       0.93
M3 (SVC Linear)             0.91       0.92       0.93       0.90       0.91
M4 (SVC RBF)                0.93       0.94       0.94       0.91       0.93
M5 (RandomForest-200)       0.94       0.95       0.96       0.93       0.94

Best Model: RandomForest (M2) with Sampling3 (30%).
License
This project is licensed under the MIT License - see the LICENSE file for details.

Author
AJAY
