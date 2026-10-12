# House Price Prediction

## Project Overview

This project predicts residential property prices using machine learning and the Bengaluru House Price dataset. It was completed as part of the QSkill Artificial Intelligence and Machine Learning internship tasks.

The notebook explores and prepares housing data, then compares three regression models: Linear Regression, Lasso Regression, and Ridge Regression.

## Internship Details

- **Organization:** QSkill
- **Domain:** Artificial Intelligence & Machine Learning
- **Task:** House Price Prediction

## Objective

To estimate a house's price using features such as:
- Location
- Total square footage
- Number of bathrooms
- Number of bedrooms (BHK)

## Dataset

- **Dataset:** Bengaluru House Price Data
- **Kaggle dataset identifier:** `amitabhajoy/bengaluru-house-price-data`
- **Download method:** The notebook uses `kagglehub` to download the dataset.
- **Target variable:** `price`

The dataset contains Bengaluru housing listings. In this dataset, prices are commonly represented in lakhs; refer to the dataset's original documentation for exact units and interpretation.

## Workflow

1. Download and load the dataset.
2. Inspect the dataset's structure, columns, and summary statistics.
3. Remove columns not used by the model.
4. Handle missing values in selected columns.
5. Convert bedroom information into a numeric BHK feature.
6. Convert square-footage ranges into numeric values.
7. Group infrequent locations and remove selected outliers.
8. Encode categorical location data and scale numeric features through preprocessing.
9. Split the data into training and testing sets.
10. Train and compare Linear Regression, Lasso Regression, and Ridge Regression.
11. Evaluate the models using Mean Squared Error (MSE) and R-squared (R²).

## Models and Saved Results

The following values are the results saved in the notebook; they have not been independently rerun for this README.

| Model | Mean Squared Error (MSE) | R² |
|---|---:|---:|
| Linear Regression | 1396.75 | 82.96% |
| Lasso Regression | 1476.50 | 81.99% |
| Ridge Regression | 1396.58 | 82.97% |

R² is the coefficient of determination, not classification accuracy. For example, an R² of 82.97% means the model explains approximately 82.97% of the variation in test-set prices relative to a baseline that predicts the mean price. MSE measures squared prediction errors, so its units are squared relative to the price unit.

Based on the saved results, Ridge Regression has the lowest MSE and highest R² among the three models, although its difference from Linear Regression is very small.

## Requirements

The notebook uses Python and libraries including:
- pandas
- NumPy
- Matplotlib
- scikit-learn
- kagglehub

Install the required libraries in your Python environment:

```bash
pip install -r requirements.txt
```

## How to Run

1. Download or clone this project.
2. Open `House Price Prediction.ipynb` in Jupyter Notebook, JupyterLab, or VS Code.
3. Install the libraries listed above.
4. Run the notebook cells in order.
5. Allow `kagglehub` to download the dataset. Depending on your Kaggle setup, you may need to configure Kaggle access or authentication.

## Conclusion

The project demonstrates a basic end-to-end house price prediction workflow, including data cleaning, feature preparation, categorical encoding, feature scaling, train-test splitting, and regression model comparison. Among the saved results, Ridge Regression performs marginally better than Linear Regression and better than Lasso Regression based on MSE and R². The results suggest that the selected housing features contain useful information for estimating prices. The scores should not be described as classification accuracy, and further validation would be needed before using the model for real-world pricing decisions.


