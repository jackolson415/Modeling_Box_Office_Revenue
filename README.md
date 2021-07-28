# Predicting Box Office Revenues

Contributors: Yasmine Hays, Tyler Pickett, Jack Olson

In this project we used a dataset from [Kaggle](https://www.kaggle.com/c/tmdb-box-office-prediction/data?select=sample_submission.csv) which contains 47 features about 3000 movies. Our goal was to create a model that could be used by movie studios to predict worldwide box office revenue. This model could be used for budgeting purposes and to see how changing movie features would affect predicted revenue. 

## EDA

1. Imputing for null values
2. Binarizing columns
3. Generating dummy columns for country, genre
4. Fixing data types to prepare for modeling

## Modeling

|                            | Training Score | Testing Score |
|----------------------------|----------------|---------------|
| 1. Linear Regression       | .6664          | .6131         |
| 2. Lasso                   | .6664          | .6131         |
| 3. Ridge                   | .6664          | .6135         |
| 4. K Nearest Neighbors     | .5669          | .4967         |
| 5. ElasticNet              | .6655          | .6187         |
| 6. Random Forest Regressor | .8145          | .6951         |


- The best performing model was a Random Forest Regressor with a maximum depth of 5
- K Nearest Neighbors performed the worst of the models, even after gridsearching for best parameters
- The performances of Linear Regression, Ridge, Lasso, and ElasticNet were all very similar

## Conclusion

Our model was able to predict about 70% of the variation in box office revenues. In the future we could increase the accuracy of our model by incorporating information about the cast, which can have a large effect on box office revenue. 
