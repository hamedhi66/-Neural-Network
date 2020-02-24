# Neural-Network

#### Introduction:

 From Alphabet Soup’s business team, a CSV containing more than 34,000 organizations that have received various amounts of funding from Alphabet Soup over the years. 

We do need to create a binary classifier that is capable of predicting whether or not an applicant will be successful if funded by Alphabet Soup using the features collected in the provided dataset 

#### Results:

Two models were used to evaluate the data: deep neural network and random forest classifier. 

For the deep neural network model the following questions were evaluated:

- How many neurons and layers did you select for your neural network model? Why? 
  - 1 input layer and 3 hidden layers were used. The number of nodes for each were 100. This number was achieved based on try and error to increase the accuracy of the model.
- Were you able to achieve the target model performance? What steps did you take to try and increase model performance?
  - Originally started with 1 input and 1 hidden layer, but increased the number of hidden layers to increase the accuracy. 
  - Originally started with 40 nodes, but to increase the accuracy of the model, the number of nodes were increased to 100.
  - 2 columns from the original data frame were dropped as they did not appear to provide any useful information to the question we try to answer. 
  - several columns from the merge data frame were dropped as they appear too have low impact on the model and could make noise to the evaluations.
  - Combine rare categorical values via bucketing.
  - Encode categorical variables using one-hot encoding.
  - Standardize numerical variables using TensorFlow’s StandardScaler class.
- If you were to implement a different model to solve this classification problem, which would you choose? Why?
  - I used the random forest classifier but I could not achieve a better accuracy. 
  -  SVM can be another option  Because if we only compare binary classification problems, SVMs have an advantage over neural network and deep learning models 
  - I may also used different scaling model rather than the standard one. 

### Summary:

What variable(s) are considered the target for your model? 
    Columns:IS_SUCCESSFUL
What variable(s) are considered to be the features for your model?
    All Columns Exept the ones being removed
What variable(s) are neither and should be removed from the input data?
    Columnnns:'IS_SUCCESSFUL','NAME','EIN'

The accuracy of the models:

​	deep neural network: 0.72, random forest classifier: 0.70