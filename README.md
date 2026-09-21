"""
# Food Order Cancellation Prediction Using Machine Learning

## Project Overview

This project uses Machine Learning to predict whether a food order is likely to be cancelled or successfully delivered.

The project uses an existing food-ordering dataset and treats the problem as a supervised binary classification problem.

## Objective

- Analyze historical food-order data
- Perform data preprocessing
- Create useful features
- Remove data leakage
- Train a Random Forest classification model
- Predict order cancellation
- Evaluate model performance
- Identify important features

## Machine Learning Type

- Learning Type: Supervised Learning
- Problem Type: Binary Classification
- Algorithm: Random Forest Classifier

## Target Variable

The target is created from the `Order Status` column.

- `0` = Delivered
- `1` = Cancelled / Unsuccessful

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook

## ML Workflow

Existing Dataset
        ↓
Data Understanding
        ↓
Data Cleaning
        ↓
Target Creation
        ↓
Leakage Removal
        ↓
Feature Engineering
        ↓
Train-Test Split
        ↓
Random Forest Classifier
        ↓
Prediction
        ↓
Model Evaluation
        ↓
Feature Importance

## Data Preprocessing

The project performs:

1. Target variable creation
2. Removal of data leakage
3. Date and time feature extraction
4. Distance conversion
5. Order item feature extraction
6. Discount feature engineering
7. Missing value handling
8. Categorical variable encoding

## Data Leakage Prevention

Features that contain information available only after the order outcome are removed.

Examples:

- Cancellation / Rejection reason
- Restaurant compensation
- Restaurant penalty
- Rating
- Review
- Customer complaint tag
- KPT duration
- Rider wait time
- Order Ready Marked

This prevents the model from using future information to make predictions.

## Model

Random Forest Classifier is used because it works well with tabular data and can capture nonlinear relationships between features.

The model uses:

- 300 trees
- Balanced class weights
- Minimum leaf size of 5

## Model Evaluation

The model is evaluated using:

- ROC-AUC
- PR-AUC
- Precision
- Recall
- F1-score
- Confusion Matrix

Accuracy is not used as the main metric because the dataset contains significantly more delivered orders than cancelled/unsuccessful orders.

## Visualizations

The project includes:

- Order Cancellation Distribution
- Confusion Matrix
- ROC Curve
- Top Feature Importance
- Actual vs Predicted Order Status

## Organization Use Case

A food-ordering organization can use the prediction system to identify orders with a higher cancellation risk.

This can help operational teams:

- Monitor high-risk orders
- Identify patterns related to unsuccessful orders
- Improve delivery operations
- Investigate operational issues
- Improve customer experience

The model provides prediction support and does not automatically prevent cancellations.

## Project Structure

Food-Order-Cancellation-Prediction/
│
├── orders.csv
├── Food_Order_Cancellation_Prediction.ipynb
└── README.md

## How to Run

Install the required libraries:

pip install pandas numpy scikit-learn matplotlib seaborn

Place `orders.csv` in the same folder as the Jupyter Notebook.

Open the notebook and run the cells sequentially.

## Future Improvements

- Hyperparameter tuning
- Model comparison
- Threshold optimization
- Streamlit deployment
- Real-time prediction API
- Model monitoring

## Conclusion

This project demonstrates how historical food-ordering data can be used to build a Machine Learning classification system for predicting unsuccessful food orders.

The project covers the complete workflow from data preprocessing and feature engineering to model training, evaluation, visualization, and business application.
"""

with open("README.md", "w", encoding="utf-8") as file:
    file.write(readme_content)

print("README.md created successfully!")
