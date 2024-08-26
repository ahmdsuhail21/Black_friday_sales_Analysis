# Black Friday Sales Analysis

## Project Overview
Black Friday, which occurs on the Friday following Thanksgiving in the United States, sees a significant surge in retail sales due to various consumer behaviors. Predicting the purchase amounts for individual customers during this period is challenging, given the complex interplay of factors such as demographics and product details. This project aims to develop a machine learning model that accurately predicts purchase amounts on Black Friday. The insights from this model can help retailers better understand consumer behavior, optimize inventory, and enhance targeted marketing strategies.

## Table of Contents
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Preparation](#data-preparation)
- [Modeling](#modeling)
- [Evaluation Metric](#evaluation-metric)
- [Conclusion](#conclusion)
- [How to Run](#how-to-run)
- [Technologies Used](#technologies-used)

## Exploratory Data Analysis (EDA)
- **Gender Analysis**: About 75% of purchases are made by male consumers, who are the primary contributors to sales. Men spend more on average compared to women, with single men spending the most.
- **Age Analysis**: Consumers aged 25-40 are the highest spenders.
- **City Stay Analysis**: Individuals who have lived in the city for just one year spend the most, likely because they are new residents who need to make new purchases.
- **City Category Analysis**: While City B contributes the most to overall sales, City C sees higher purchases of specific products.

## Data Preparation
- **Label Encoding**: Categorical columns like Age, Gender, and City_Category were encoded using `LabelEncoder`.
- **Dummy Variables**: The `Stay_In_Current_City_Years` feature was converted into dummy/indicator variables using `get_dummies` from Pandas.
- **Handling Missing Values**: Missing values in Product_Category_2 and Product_Category_3 were filled.

## Modeling
- The dataset was split into an 80:20 ratio for training and testing.
- Implemented multiple supervised models including:
  - Linear Regression
  - Decision Tree Regression
  - Random Forest Regression
  - XGBoost Regression

## Evaluation Metric
The model's performance was evaluated using **Root Mean Square Error (RMSE)**, which measures the average squared difference between predicted and actual values. RMSE is a standard metric for assessing the accuracy of predictive models for quantitative data.

## Conclusion
Among the models implemented, **XGBoost Regression** performed the best with an RMSE score of **2853**. This model is effective in predicting Black Friday purchase amounts based on the given features.

## How to Run
1. Clone the repository:
    ```bash
    git clone https://github.com/ahmdsuhail21/Black_friday_sales_Analysis.git
    ```
2. Navigate to the project directory:
    ```bash
    cd Black_friday_sales_Analysis
    ```
3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
4. Run the Jupyter Notebook to explore the analysis and model implementation:
    ```bash
    jupyter notebook Black_Friday_Sales_Analysis.ipynb
    ```

## Technologies Used
- Python
- Pandas
- Scikit-learn
- XGBoost
- Jupyter Notebook
