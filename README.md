# car_breakdown prediction

## Approch Followed
1. Converted problem to classification problem: to predict if car will(not) breakdown within 30 days of present day
2. Steps:
    1. Data Preparation: Calculate RUL for each vehicle from train/test set, if RUL is below 30 then label the entry as True indicating car will breakdown.
    2. Data Exploration:(present in car_breakdown_prediction-Copy1.ipynb). Find correlations between various independent variables (very few variables with > 0.8 correlation)
    3. Feature engineering: 
        i. remove features which do not vary across the training set
        ii. added rolling window mean, std and diff features
    4. Used Logistic regression model for training. 
     
     
Other approaches/improvements to current approach:
  1. use of PCA for dimensionality reduction and feature selection
  2. comparison with other classifiers like RandomForest, xgboost etc
  3. Same problem can be solved as regression problem to predict RUL, since provided dataset is very small it is better to convert the problem to classification.
     
