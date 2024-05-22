# Housing Price Prediction

## About
A US-based housing company named Surprise Housing has decided to enter the Australian market. The company uses data analytics to purchase houses at a price below their actual values and flip them on at a higher price. For the same purpose, the company has collected a data set from the sale of houses in Australia. The data is provided in the CSV file below.
The company is looking at prospective properties to buy to enter the market. You are required to build a regression model using regularisation in order to predict the actual value of the prospective properties and decide whether to invest in them or not.
The company wants to know:
Which variables are significant in predicting the price of a house, and
How well those variables describe the price of a house.
Also, determine the optimal value of lambda for ridge and lasso regression.

## Business Goal
You are required to model the price of houses with the available independent variables. This model will then be used by the management to understand how exactly the prices vary with the variables. They can accordingly manipulate the strategy of the firm and concentrate on areas that will yield high returns. Further, the model will be a good way for management to understand the pricing dynamics of a new market.
## Methodology
1. **Data Preprocessing**
   - Handling missing values by imputing median for numerical columns and 'None' for categorical columns.
   - Encoding categorical variables using one-hot encoding.
   - Scaling features using MinMaxScaler.
   - Splitting the data into training and testing sets.

2. **Model Building**
   - **Linear Regression**: Built a basic linear regression model with Recursive Feature Elimination (RFE).
   - **Ridge Regression**: Applied Ridge regression with cross-validation to determine the optimal value of alpha.
   - **Lasso Regression**: Applied Lasso regression with cross-validation to determine the optimal value of alpha.

3. **Evaluation Metrics**
   - Evaluated the models using R2 Score, RSS (Residual Sum of Squares), and MSE (Mean Squared Error) on both training and testing sets.

## Results

### Linear Regression
| Metric              | Value                |
|---------------------|----------------------|
| R2 Score (Train)    | 0.75                 |
| R2 Score (Test)     | 0.62                 |
| RSS (Train)         | 1,736,000,291,646.84 |
| RSS (Test)          | 856,453,961,018.30   |

### Lasso Regression
| Metric              | Value                |
|---------------------|----------------------|
| R2 Score (Train)    | 0.89                 |
| R2 Score (Test)     | 0.88                 |
| RSS (Train)         | 763,423,313,686.70   |
| RSS (Test)          | 272,954,682,056.98   |

### Ridge Regression
| Metric              | Value                |
|---------------------|----------------------|
| R2 Score (Train)    | 0.90                 |
| R2 Score (Test)     | 0.87                 |
| RSS (Train)         | 729,049,310,188.63   |
| RSS (Test)          | 292,067,677,438.38   |



## Conclusion
The Lasso Regression model with optimal alpha value is used  as the best model for predicting housing prices in the Australian market.
