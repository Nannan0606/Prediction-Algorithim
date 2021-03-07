# Covid-19 Predictive Algorithm challenge
## This is a Hackathon challenge group project. Huge thanks to the teammembers (Team Monks). 

Obtained from a public datasets by NYT. The dataset contains the following features: county, state, fips, cases, deaths, region

The goal of the project is to develop a predictive algorithm to predict the number of positive cases in the US between 7/27/20 - 8/15/20.

## Modelling
We used an RNN model for this. We defined a class called RNN with specified parameters - input_size, output_size, hidden_di and n_layers. Then we generate evenly spaced, test data points with about 30% size; which created our train and test tensors.

Input size: [1, 186, 3]
Output size: [186, 1]
Hidden state size: [2, 1, 10]
Then we instantiate an RNN after tuning its hyperparametes a little and we choose an MSE loss and Adam optimizer with a learning rate of 0.01.

## Training
Then comes the training part. We trained our model with 100 epochs and printing the model every 15epochs which totals to about 5 graphs. Our loss started with 0.9663447141647339 and ended with a final loss % of 0.01163563597947359
