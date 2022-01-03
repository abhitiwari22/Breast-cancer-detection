# Breast-cancer-detection using ann

Breast cancer is the second leading cause of cancer deaths worldwide and occurrs in one out of eight women.
# dataset 
It is available on kaggle.
In this dataset, we point to the ‘diagnosis’ feature column, so we check the value count of that column using pandas:
After that I have  visualize the value counts of the ‘diagnosis columns: for the better understanding
Null Values
In the dataset, I have  check that null values that are present inside the variables for that we use pandas:
After executing the program we reach the conclusion that the feature name ‘Unnamed:32’ contains all the null values so we delete or drop that column.
# Independent and Dependent Variables
Divided the dataset into independent and dependent variables, for that we create two variables one represents independent and the other represents dependent.
# Splitting Data
Splitting the data into training and testing parts:
This article was published as a part of the Data Science Blogathon
# Scaling the Data
I have created the artificial neural network, then  scale the data into smaller numbers because the deep learning algorithm multiplies the weights and input data of the nodes and it takes lots of time, So for reducing that time we scale the data.

After importing libraries, I create the three types of layers:

Input layer
Hidden layer
Output layer
First, we create the model:

#creating model
classifier = Sequential()
A sequential model is appropriate for a plain stack of layers where each layer has exactly one input tensor and one output tensor.

Now we create the layers of the neural network:
#have a look in notebook
After executing this code we take the summary of it using :

#taking summary of layers
classifier.summary()

Compiling ANN
Now we compiling our model with the optimizer:

#compiling the ANN
Fitting the ANN Into Training Data
After compiling the model we have to fit the ANN into the training data for the prediction:

#fitting the ANN to the training set
model = classifier.fit(xtrain,ytrain,batch_size=100,epochs=100)
model training
The fit() method fits the ANN to the training data, in the parameters we set the specific values of each variable like batch_size, epochs, etc… At last, we find an excellent accuracy score, So our model fir perfectly into training data.

After training data we have to test the accuracy score for the Test data also, let’s see below:

#now testing for Test data
notebook
On executing this code we find that y_pred contained the different values so we converting the predicting values into the threshold values like True, False.

Score and Confusion Matrix
Now we check the confusion matrix and the score of the predicted values.

 take a look in notebook






# Conclusion
ANNs help physicians in diagnosing acting as a powerful tool. It has been proven suitable for satisfactory diagnosis and medical decision making of various other              medical conditions.
Despite their wide application in medical diagnosis they must be considered as a final tool for decision making of the condition to the physician, who will be finally   responsible for eventually interpreting the output of the artificial neural network.
The neural networksbased clinical support systems provide the medical experts with a second opinion thus removing the need for biopsy, excision and reduce the unnecessary expenditure.
