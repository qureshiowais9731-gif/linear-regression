Housing Price Prediction: Simple & Multiple Linear Regression

This repository contains a Python script (linear_regression_housing.py) that demonstrates the implementation and evaluation of both Simple Linear Regression (SLR) and Multiple Linear Regression (MLR) models using the Scikit-learn library, Pandas for data handling, and Matplotlib for visualization.

The objective is to predict house prices based on various features from the included Housing.csv dataset.

📊 Objective

To compare the performance of:

Simple Linear Regression: Predicting house price using only the area feature.

Multiple Linear Regression: Predicting house price using a comprehensive set of features, including area, bedrooms, bathrooms, and other categorical amenities.

🛠️ Tools & Libraries

The following Python libraries are required to run the analysis:

Pandas: For data loading, manipulation, and preprocessing.

NumPy: For numerical operations (used implicitly by Pandas and Scikit-learn).

Scikit-learn (sklearn): For model training (LinearRegression), data splitting (train_test_split), and evaluation metrics (MAE, MSE, R²).

Matplotlib: For visualizing the simple linear regression line.

🚀 Setup and Execution

The provided script is optimized for execution in a Google Colab environment, which simplifies the process of uploading the required CSV file.

Prerequisites

You need the Housing.csv file in the same directory as the script (or upload it in Colab).

A. Running in Google Colab (Recommended)

Open Google Colab: Create a new Python notebook in Google Colab.

Copy Code: Copy the entire content of linear_regression_housing.py into a single cell in the notebook.

Run Cell: Execute the cell.

Upload File: When prompted by the files.upload() command, click the "Choose Files" button and select the Housing.csv file from your local machine.

View Output: The script will execute the analysis and display the evaluation metrics and the regression plot.

B. Running Locally (e.g., VS Code, Jupyter)

If running locally, ensure Housing.csv is in the same directory as the script. You will need to comment out or remove the Colab-specific block at the end:

# --- MAIN EXECUTION BLOCK FOR COLAB ---
# if COLAB_ENV:
# ... (remove this block for local execution)
# else:
#     # Fallback execution for non-Colab environments
#     print("Running in a non-Colab environment. Assuming file is local.")
#     run_linear_regression_analysis(FILE_NAME)


🔍 Key Results and Interpretation

The script provides detailed output for both models, but the key metric to compare is the R-squared ($R^2$) value:

1. Simple Linear Regression (SLR)

R²: Measures how well the single feature (area) explains the variance in price.

Interpretation: The output will show the regression equation: Price = Intercept + Coefficient * Area. The coefficient indicates the change in price for every one unit increase in area.

2. Multiple Linear Regression (MLR)

R²: Measures how well all features (area, bedrooms, bathrooms, mainroad, etc.) collectively explain the variance in price.

Pre-processing: Categorical features (like mainroad, furnishingstatus) are converted into numerical dummy variables using pd.get_dummies() before fitting the model.

Comparison: The R² value for the MLR model should be significantly higher than the SLR model, demonstrating that considering additional features vastly improves the model's predictive power.

🤝 Next Steps

Explore feature scaling (e.g., StandardScalar) for the MLR model.

Implement regularization techniques (Ridge or Lasso) to potentially improve generalization.

Analyze the residuals (the differences between actual and predicted values) for homoscedasticity.
