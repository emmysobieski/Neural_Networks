Neural Networks Challenge

I first prepared the data by removing unique identifiers EIN and Name and Status (which is always 1).  I then created buckets for Classification and Application type.  Once these buckets were created, then I ran OneHotEncoder to encode data, and then scaled the data.  I used sigmoid output activation funtion because the result is binary: is the investment successful or not?

I created several neural nets:

1. 2 layers, 8 neurons, 5 neurons, ReLU for input activation function, sigmoid output activation function, 25 Epochs ==> 72.47 accuracy

2. 2 layers, 40 neurons, 8 neurons, ReLU for input activation function, sigmoid output activation function, 50 Epochs ==> 72.7 accuracy ***BEST MODEL

3. 1 layers, 48 neurons, 5 neurons, ReLU for input activation function, sigmoid output activation function, 50 Epochs ==> 72.47 accuracy

4. 2 layers, 8 neurons, 5 neurons, tanh for input activation function, sigmoid output activation function, 50 Epochs ==> 72.58 accuracy

5. 2 layers, 8 neurons, 5 neurons, ReLU for input activation function, sigmoid output activation function, 50 Epochs ==> 72.59 accuracy (better with more Epochs)

To try to increase model performance, I bucketed data where appropriate, encoded and then scaled the data.  With the model itself, I changed activation functions, changed number of neurons, number of layers, and number of epochs, and tried different combinations of these changes.

Target model performance of 75% was NOT acheived, however I did come close at 72.7% for my best model (#2 above).  This model had two layers, 40 neurons in the first input layer, 8 neurons in the second input layer, used ReLU for both input activation functions, and used sigmoid for the output activation function, and ran for 50 Epochs.

I would use Random Forest as a classification model, because this data seems to be stronger as an ensemble which is what Random Forest does well - takes alot of weak correlations and together makes a stronger predictive model.
