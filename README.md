# UCM Regression for Calculating Elasticity

This Python code performs UCM (Unobserved Components Model) regression for calculating elasticity. The code takes a dataset as input and performs various data preprocessing steps, followed by UCM regression analysis. The dataset is assumed to be in a CSV format.

### Prerequisites
Before running the code, ensure that the following Python libraries are installed:

pandas
numpy
seaborn
matplotlib
sklearn
statsmodels
Code Overview
The code performs the following steps:

Importing necessary libraries: The required libraries for data processing and UCM regression are imported.

Loading the dataset: The code loads the dataset from the "ucm_week_sun.csv" file and assigns it to the variable df.

Data preprocessing: The code performs several data preprocessing steps, including adding a new column 'total_paid' based on existing columns, handling missing values, and categorizing the 'GRIFOLS_TOTAL_PAID' column.

Computing average price: The code calculates the average price by grouping the dataset based on 'site_code', 'week_end_sun', and 'GRIFOLS_TOTAL_PAID' columns.

Grouping total donations: The code groups the dataset by 'site_code' and 'week_end_sun' to compute the total number of donations.

Merging datasets: The code merges the datasets obtained from the previous steps to create the final dataset for regression analysis.

Regression analysis: The code performs both ordinary linear regression and UCM regression. For ordinary linear regression, it computes the regression coefficients for each site and variable. For UCM regression, it fits an Unobserved Components Model to each site's data and computes the regression coefficients.

Output: The code stores the regression results in two separate CSV files named 'UCM_result_v1.csv' and 'Regression_result_v1.csv'.

### Usage
To use this code, follow these steps:

Ensure that the required libraries are installed.

Prepare your dataset in a CSV file with the appropriate column names and formats.

Update the code to specify the correct file paths for loading and saving the dataset.

Run the code.

The regression results will be saved in the 'UCM_result_v1.csv' and 'Regression_result_v1.csv' files.

Note: This code assumes that the input dataset and site matching file ('site_match.csv') are available in the specified file paths.

### Additional Notes
The code applies UCM regression to calculate elasticity, which can provide insights into the relationship between variables in the dataset.
The UCM regression assumes an unobserved components model with both level and irregular components.
The ordinary linear regression is performed using the LinearRegression class from scikit-learn library.
The UCM regression is performed using the UnobservedComponents class from statsmodels library.
