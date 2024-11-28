# classification-challenge

## Project Overview

Project using logistic regression and random forest models for spam detectors.

## Data Source

The data is located at [https://static.bc-edx.com/ai/ail-v-1-0/m13/challenge/spam-data.csv](https://static.bc-edx.com/ai/ail-v-1-0/m13/challenge/spam-data.csv)

Dataset Source: [UCI Machine Learning Library](https://archive.ics.uci.edu/dataset/94/spambase)

## Script Breakdown

CSV file imported from a URL and displays the first five rows of the dataset.

### Spam Detector:
Read the data from the given URL into a Pandas DataFrame named data. The URL points to the location of the dataset, in this case, a CSV file. Displayed the first five rows of the DataFrame. This is helpful for understanding the structure of the dataset, including the column names, data types, and some sample values.

### Split the Data into Training and Testing Sets:

1. Created the labels set y and features DataFrame X from the dataset, splitting the data into the dependent variable (y) and the independent variables (X).

    X = data['Text']: Creates a DataFrame or Series containing only the Text column, which holds the actual message content.

    y = data['Label']: Creates a Series containing the Label column, which indicates whether the message is spam or ham.

2. Checked the balance of the labels in y using the value_counts() function to see the distribution of the classes.

    y.value_counts(): Counts the number of occurrences of each unique value in the y Series.
   
3. Split the dataset into training and testing sets.

   test_size=0.2: Allocates 20% of the data to the testing set and 80% to the training set.
   
    random_state=42: Ensures reproducibility by setting a random seed for the split.
   
    X_train and y_train: Used for training the model.
   
    X_test and y_test: Used for evaluating the model.

4. Used the StandardScaler to scale the features data.
   
    Created the Standard Scaler with the training data

    Fit the Standard Scaler with the training data
  
    Scale the training data
   
### Create Logistic Regression Model: Created a Logistic Regression model, fit it to the training data, made predictions with the testing data, and print the model's accuracy score.  

1. Trained a logistic regression model and printed the model score
 
2. Made and saved the testing predictions with the saved logistic regression model using the test data
 
3. Reviewed the predictions
  
4. Calculated the accuracy score by evaluating 'y_test' vs. 'testing_prediction"

### Create Random Forest Model: Created a Random Forest Classifier model, fit it to the training data, made predictions with the testing data, and printed the model's accuracy score. 

1. Trained a Random Forest classifier model and printed the model score.

2. Made and saved testing predictions with the saved logistic regression model using the test data.

3. Reviewed the predictions.

4. Calculated the accuracy score by evaluating 'y_test' vs. 'testing_predictions'

### Evaluted the Models

Determined which model performed better.
