### 21. deep-learning-challenge 
# Charity Funding Predictor

## Overview
### The goal of this project is to create an algorithm using machine learning and neural networks to predict whether applicants will be successful if funded by the fictional non-profit foundation, Alphabet Soup.
----------------------------
----------------------------

## Process
I was given a CSV file that I read into Pandas. This file contained more than 34,000 organizations that have received funding from the fictional foundation along with several columns of metadata about each organization.

PREPROCESSING<br>
I preprocessed the data by:
* dropping non-beneficial columns,
* finding the number of data points for each unique value for each of the columns that had more than 10 unique values - APPLICATION_TYPE and CLASSIFICATION,
* choosing a cutoff point of 600 and 300, respectively, to bin rare categorical values together into a new value called "Other",
* using `pd.get_dummies()` to convert categorical data to numeric,
* dividing the data into a target array (IS_SUCCESSFUL) and features arrays,
* applying the `train_test_split` to create a testing and a training dataset,
* and finally, using `StandardScaler` to scale the training and testing sets

The resulting data included 44 features. The target variable (y) was IS_SUCCESSFUL. The data was split into training and test subsets.

COMPILING, TRAINING, AND EVALUATING THE MODEL<br>
The model was required to achieve a target predictive accuracy higher than 72%. I made three official attempts using machine learning and neural networks. They all resulted in the same accuracy rate – right around 72%, so a little short of the required target accuracy.

Results from each model attempt are detailed below:

ATTEMPT 1<br>
The first attempt resulted in an <b>accuracy score of 73.3%. This was the highest accuracy score of the three models.</b> This means that 72.8% of the model’s predicted values align with the dataset’s true values.

The hyperparameters used were:
* layers = 2
  * layer1 = 8 neurons : activation function = ‘relu’
  * layer2 = 5 neurons : activation function = ‘relu'
* epochs = 100


ATTEMPT 2<br>
For my second attempt resulted in an <b>accuracy score of 73.2%.</b> This means that 73.2% of the model’s predicted values align with the dataset’s true values.

The hyperparameters used were:
* layers = 2
  * layer1 = 10 neurons : activation function = ‘relu’
  * layer2 = 10 neurons : activation function = ‘relu’
  
* epochs = 100


ATTEMPT 3<br>
For my third and final attempt resulted in an <b>accuracy score of 46.7%.</b> This means that 46.7% of the model’s predicted values align with the dataset’s true values.

The hyperparameters used were:
* layers = 2
  * layer1 = 20 neurons : activation function = ‘relu’
  * layer2 = 20 neurons : activation function = ‘sigmoid’
                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      
* epochs = 100

## Summary
In the three attempts I made, first two model was able to achieve a target predictive accuracy higher than 72%. Using a model with greater correlation between input and output would likely result in higher prediction accuracy. This could be achieved by doing additional data cleanup up front, as well as by using a model with different activation functions and iterating until higher accuracy is reached.

