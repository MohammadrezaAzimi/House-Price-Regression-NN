# House-Price-Regression-NN

# Project description: 
In this project, the price of house in the suburb of Boston in mid-1970 is described as a function of 13 features such as crime rate, tax, etc. Training and test sets are comprised of 404 and 102 samples, respectively.

# Network model: 
A three-layer neural network is used. The network is comprised of two fully-connected layers with 64 hidden units and rectified linear unit (ReLU) activation as well as the output layer with no activation (a linear layer). 

# Details: 
Optimization of stochastic gradient descent algorithm is done using RMSProp. Mean absolute value is performance metric and mean square error is the loss function. Since the size of training set is small, K-fold cross-validation (K=4) is used. Here are the tips for implementation:

1- Mean and standard deviation of training data are computed and then are used for normalizing both training and test data.

2- The model is defined in terms of a function to be called in each iteration of K-fold cross-validation.

3- By setting K=4, at each iteration 1/4 of training data is used as validation data while the rest is used for training the model and then MSE and MAE of the model is evaluated on the validation set.

4- Running the model for 100 epochs, results in average validation score of 3000$ which is the payoff of buying a house using the learned model.

5- The model is run for 500 epochs.

# Modification:
Since the validation MAE stops improving after 80 epochs, the model is trained only for 80 epochs and then is used for prediction.
