### Overview
This Jupyter Notebook applies a Logistic Regression model to classify loan applicants into two categories:

0 (Healthy Loan): Low-risk applicants who are likely to repay their loans.
1 (High-Risk Loan): High-risk applicants who are at risk of defaulting on their loans.

### Dataset
The dataset includes various features related to loan applications, such as financial indicators, borrower details, and credit history. The target variable is funding_status, where:

0 represents a healthy loan (low risk).
1 represents a high-risk loan.

### Workflow
The notebook follows these steps:

- 1. Data Loading and Preprocessing
* Import the CSV data into a Pandas DataFrame.
* Identify and address any missing values in the dataset.
Separate the data into features (X) and target labels (y).
- 2. Data Splitting
* Use train_test_split to divide the data into training (80%) and testing (20%) sets, ensuring reproducibility by setting random_state=1.
- 3. Logistic Regression Model Training
* Instantiate a Logistic Regression model from sklearn.linear_model.
* Train the model using the training data (X_train, y_train).
- 4. Making Predictions
* Generate predictions on the test data (X_test) using the trained model.
- 5. Model Evaluation
* Generate a confusion matrix to evaluate the accuracy of the predictions.
* Print a classification report to assess key metrics like precision, recall, and F1-score.

### Model Performance
- Classification Report:
* Healthy Loan (0): Precision = 1.00, Recall = 0.99, F1-score = 1.00
* High-Risk Loan (1): Precision = 0.84, Recall = 0.94, F1-score = 0.89
* verall Accuracy: 99%
### Confusion Matrix 
[[18655, 110] [ 36, 583]]
* 18655 True Negatives: Healthy loans correctly identified as healthy.
* 583 True Positives: High-risk loans correctly identified as high-risk.
* 110 False Positives: Healthy loans misclassified as high-risk.
* 36 False Negatives: High-risk loans misclassified as healthy.

### Key Insights
* The model performs excellently in identifying healthy loans, with near-perfect precision.
* It also performs well on high-risk loans, though the precision (84%) is slightly lower, meaning some healthy loans are misclassified as high-risk.
* The model has a high recall (94%) for identifying high-risk loans, ensuring that most high-risk cases are detected.

### Potential Improvements
* Feature Engineering: Introduce new features or refine existing ones to better differentiate high-risk borrowers.
* Hyperparameter Tuning: Test different regularization strengths to achieve a better balance between precision and recall.
* Resampling Techniques: Address any class imbalances in the dataset using methods like SMOTE (Synthetic Minority Over-sampling Technique).

### Dependencies
* This notebook requires the following Python libraries:

- pandas
- numpy
- sklearn

### How to Use
1) Clone or download the repository and open the notebook.
2) Ensure all dependencies are installed by running:
   - pip install pandas numpy scikit-learn
3) Run all cells in the notebook to train and evaluate the model.

### Author

This notebook was developed to analyze credit risk classification using machine learning techniques.



