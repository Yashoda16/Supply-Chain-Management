# Supply-Chain-Management
This project aims to optimize the supply quantity of instant noodles to various warehouses across the country for an FMCG company. The mismatch between high demand and low supply has caused inventory cost losses. This model uses historical data to determine the optimum product weight to be shipped to each warehouse. Additionally, the project analyzes demand patterns in different regions to help the management drive more targeted advertisement campaigns.

# Table of Contents
### 1. Project Overview
### 2. Project Workflow
      1. Data Exploration and Understanding
      2. Data Preprocessing
      3. Feature Selection
      4. Model Development
      5. Model Evaluation
      6. Deployment Recommendation
      7. Demand Analysis for Marketing Strategy
### 3. Technologies Used
### 4. How to Use
## Project Overview
The inventory management problem in the FMCG company's instant noodle business stems from the inability to match supply with fluctuating demand, leading to financial losses. The objective of this project is two-fold:

    Build a predictive model to optimize the amount of product to be shipped to various warehouses.
    Analyze demand patterns across different geographical pockets to inform advertisement strategies.
## Project Workflow
1. Data Exploration and Understanding: Explore the dataset to gain insights into the characteristics of the data using data.info(). This method prints a summary that includes:
The total number of entries (rows).
The number of non-null values for each column.
The data type of each column.
The memory usage
This information is useful for identifying potential data quality issues such as missing values and understanding the overall structure of the dataset. 

2. Data Preprocessing:
This phase focuses on preparing the data for modeling.

Steps involved:

    Handling Missing Data: Filling in or removing missing values appropriately.

    Outlier Detection: Identifying and handling outliers in shipment and demand data.

    Normalization/Scaling: Standardizing data to ensure models perform optimally.

    Categorical Encoding: Converting categorical variables into numerical form using methods like one-hot encoding or label encoding.

The preprocessed data ensures the model performs well without biases from poor data quality.

3. Feature Selection:
In this step, we perform feature engineering to select the most relevant variables for predicting shipment quantities. Techniques such as correlation analysis and feature importance ranking are used to determine which features contribute the most to the model's predictions.

Some key features selected for the model include:

    Warehouse Capacity
    Historical Demand Patterns
    Seasonality/Trends
    Geographical Features
    
4. Model Development:
We used regression models to predict the optimum shipment quantity. The following algorithms were explored due to their strong predictive performance:

    LightGBM
   
    Random Forest
   
    CatBoost
   
Each model was trained on the preprocessed data and evaluated using cross-validation.

5. Model Evaluation:
The models' performance was evaluated using Mean Squared Error (MSE) as the primary metric. Cross-validated MSE across models showed the following results:

LightGBM: MSE ~758,581.72

Random Forest: MSE ~758,581.72

CatBoost: MSE ~758,581.72

The models show good generalization to new data, with close training and testing metrics. Additionally, the MSE values represent a significant improvement over a baseline model.

6. Deployment Recommendation:
Given the model performance, it is recommended to deploy LightGBM, Random Forest, or CatBoost to predict the optimal product weight to ship to each warehouse. These models generalize well, showing no significant overfitting, and can make robust predictions on new, unseen data.

7. Demand Analysis for Marketing Strategy:
After evaluating demand patterns across different regions, the data shows consistent demand across zones:

Mean and Median Values: The average and median demand is similar across regions.
Standard Deviation: There is little variability in demand, suggesting a balanced distribution across zones.
These insights suggest that management can run more generalized advertisement campaigns, or choose to target specific zones based on the company's marketing strategy.

## Technologies Used
Python: Data analysis and modeling.

Pandas: Data manipulation and preprocessing.

Scikit-learn: Model training and evaluation.

LightGBM, Random Forest, CatBoost: Regression models for predictive analysis.

Matplotlib, Seaborn: Data visualization.

Jupyter Notebook: For code development and experimentation.

