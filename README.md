# Deep_Learning_Challenge


Instructions:

# Step 1: Preprocess the Data

* Read in the charity_data.csv to a Pandas DataFrame, and be sure to identify the following in your dataset:
* What variable(s) are the target(s) for your model?
* What variable(s) are the feature(s) for your model?
* Drop the EIN and NAME columns.
* Determine the number of unique values for each column.
* For columns that have more than 10 unique values, determine the number of data points for each unique value.
* Use the number of data points for each unique value to pick a cutoff point to bin "rare" categorical variables together in a new value, Other, and then check if the binning was successful.
* Use pd.get_dummies() to encode categorical variables.
* Split the preprocessed data into a features array, X, and a target array, y. Use these arrays and the train_test_split function to split the data into training and testing datasets.
* Scale the training and testing features datasets by creating a StandardScaler instance, fitting it to the training data, then using the transform function.

# Step 2: Compile, Train, and Evaluate the Model

* Continue using the file in Google Colab in which you performed the preprocessing steps from Step 1.
* Create a neural network model by assigning the number of input features and nodes for each layer using TensorFlow and Keras.
* Create the first hidden layer and choose an appropriate activation function.
* If necessary, add a second hidden layer with an appropriate activation function.
* Create an output layer with an appropriate activation function.
* Check the structure of the model.
* Compile and train the model.
* Create a callback that saves the model's weights every five epochs.
* Evaluate the model using the test data to determine the loss and accuracy.
* Save and export your results to an HDF5 file.

# Step 3: Optimize the Model
* Attempt to get the model to run with an accuracy over 75%

# Step 4 Results:
Data Preprocessing

* What variables are the targets for your model?
  - "Is_Successful" was the variable used as the main indictor to see if the charity funds will be allocated correctly by using the model
* What variable(s) are the features for your model?
  - Application_Type, Status, Income_AMT, Special_Considerations, ASK_AMT, and Afflication were used as features for the model.
*What variable(s) should be removed from the input data because they are neither targets nor features?
  - Name and EIN were removed since they were not applicable

Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
   - For the first model I chose 2 hidden layers with 100 and 50 neaurons since that is about 2 1/2 times of the input features
* Were you able to achieve the target model performance?
 - I was not unforutnatley. I tried many combinations and could only improve by about 1/2 a percent
* What steps did you take in your attempts to increase model performance?
  - I attempted to increase the number of layers, increase & decrease the number of epochs, drop columns, and modify the bins

# Summary

Overall the model was able to get close to a 75% accuracy, my highest optimal accuracy being .7450 which I think is an acceptable basis to make anayltic decisions based off of the results. I found that adding more hidden layers actually decreased the accuracy of the model and that for me it perfomed best with 3 layers. 


