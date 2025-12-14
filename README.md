# 📈 **Linear Regression Workflow using KNIME Analytics Platform**

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 📌 **[Project Overview](https://github.com/ankitaanand96/linear_regression_knime_workflow/blob/main/Linear%20Regression%20KNIME%20Workflow.png)**

This project demonstrates an end-to-end Linear Regression workflow built using the KNIME Analytics Platform to predict sales revenue based on multiple business and operational features. The workflow covers the complete data science lifecycle — from data cleaning and preprocessing to model training, prediction, and evaluation. Special attention is given to handling missing values, converting data types, and ensuring the dataset is suitable for regression modeling. The final output evaluates model performance using standard regression metrics such as RMSE, MAE, and R².

The project is implemented using KNIME’s no-code / low-code approach, making it easy to understand and reproduce even for users without strong programming backgrounds.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## **About KNIME Analytics Platform**

KNIME Analytics Platform is an open-source, visual data science tool that allows users to build analytics and machine learning workflows using drag-and-drop nodes instead of writing code. Each node represents a specific task such as data reading, cleaning, transformation, modeling, or evaluation.

KNIME is widely used in industry and academia because it:

- Makes data science accessible to non-programmers

- Provides transparency and reproducibility in workflows

- Supports advanced analytics, machine learning, and AI

- Integrates easily with Python, R, SQL, and big data tools

This project showcases how KNIME can be used to build a robust regression model step by step without writing a single line of code.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🔁 **Workflow (Step-by-Step)**

### 1️⃣ **[Convert “?” to Missing Values (Data Cleaning)](https://github.com/ankitaanand96/linear_regression_knime_workflow/blob/main/Column%20Expression%20Configuration.png)**

Real-world datasets often represent missing values using symbols like "?".

This step converts all "?" entries into proper null (missing) values so that KNIME can recognize and handle them correctly in later steps.

Why this is important:

Models cannot work with text symbols in numeric columns.

### 2️⃣ **[Missing Value Column Filter (Feature Selection)](https://github.com/ankitaanand96/linear_regression_knime_workflow/blob/main/Missing%20Value%20Column%20Filter%20Configuration.png)**

This node removes columns that contain too many missing values (for example, more than 40%).

Columns with excessive missing data usually add noise and reduce model quality.

Why this is important:

Keeps only meaningful and reliable features for training the regression model.

### 3️⃣ **[Missing Value Node (Imputation)](https://github.com/ankitaanand96/linear_regression_knime_workflow/blob/main/Missing%20Value%20Configuration.png)**

After removing bad columns, remaining missing values are handled using statistical methods:

- Numeric columns → replaced using Median

- Categorical/String columns → replaced using Most Frequent Value

Why this is important:

Ensures the dataset has no missing values before model training.

### 4️⃣ **[Column Auto Type Cast (Data Type Fixing)](https://github.com/ankitaanand96/linear_regression_knime_workflow/blob/main/Column%20Auto-Type%20Cast%20Configuration%20.png)**

This node automatically converts columns to the correct data types (e.g., String → Double).

Linear Regression requires numeric inputs, so this step ensures compatibility.

Why this is important:

Prevents errors during model training caused by incorrect data types.

### 5️⃣ **[Table Partitioner (Train–Test Split)](https://github.com/ankitaanand96/linear_regression_knime_workflow/blob/main/Table%20Partitioner%20Configuration.png)**

The cleaned dataset is split into:

i. Training set (e.g., 70%)

ii. Testing set (e.g., 30%)

Why this is important:

Allows the model to be trained on one portion of data and evaluated on unseen data.

### 6️⃣ **[Linear Regression Learner (Model Training](https://github.com/ankitaanand96/linear_regression_knime_workflow/blob/main/Linear%20Regression%20Learner%20Configuration.png)**

This node trains a Linear Regression model using the training dataset.

It learns the relationship between multiple input features and the target variable Sales_Revenue.

Why this is important:

This is the core machine learning step where the predictive model is created.

### 7️⃣ **[Regression Predictor (Prediction)](https://github.com/ankitaanand96/linear_regression_knime_workflow/blob/main/Regression%20Predictor%20Configration.png)**

The trained model is applied to the test dataset to generate predictions.

[A new column (Predicted Sales_Revenue) is added to the output.](https://github.com/ankitaanand96/linear_regression_knime_workflow/blob/main/Regression%20Predictor%20Table.png)

Why this is important:

Shows how well the model can predict unseen data.

### 8️⃣ **[Numeric Scorer (Model Evaluation)]([https://github.com/ankitaanand96/linear_regression_knime_workflow/blob/main/Numeric%20Scorer%20Configuration.png)**

[The model’s performance is evaluated using regression metrics such as:](https://github.com/ankitaanand96/linear_regression_knime_workflow/blob/main/Numeric%20Scorer%20Statistics%20.png)

- R²

- RMSE

- MAE

Why this is important:

Helps measure prediction accuracy and overall model quality.

### 9️⃣ **[Visualization](https://github.com/ankitaanand96/linear_regression_knime_workflow/blob/main/Visualisation%20Chart.png)**

- A scatter or line plot can be created to visually compare:

- Actual Sales_Revenue vs Predicted Sales_Revenue

Why this is important:

Makes model performance easier to understand visually.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## ✅ **Key Learnings from This Workflow:**

i.  How to clean and preprocess real-world datasets.

ii. How to handle missing values correctly.

iii. How to train and evaluate a Linear Regression model.

iv. How no-code tools like KNIME replicate full ML pipelines used in Python/R.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🛠 **Tools Used:**

- KNIME Analytics Platform

- Linear Regression

- Statistical Imputation

- Train–Test Validation

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🚀 **Use Case:**

This workflow can be reused for:

- Sales forecasting

- Revenue prediction

- Cost estimation

- Business analytics projects

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------
