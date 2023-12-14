# Diabetes Machine Learning Project

![GitHub Logo](https://medlineplus.gov/images/Diabetes_share.jpg)

## Objective
Diabetes affects almost 40 million people in the US alone. A good predictive model based on patient demographics can help doctors and patients with early intervention and preventative treatments. 

## Data
Data was retrieved from (https://www.kaggle.com/datasets/julnazz/diabetes-health-indicators-dataset) and came with 3 datasets; 2 unbalanced and 1 balanced. The balanced one was chosen to optimize for model accuracy and to ensure that our predictions actually predicted diabetes.

## Methods
A database was created in SQL which was then conected to a python notebook using SQLite. Using numpy, pandas, and seaborn, the data was assessed and visualized. Next, a tensorflow model was created to predict outcome of Diabetes.

We cleaned the data with pandas, including changing datatypes to be the correct types, as well as dropping some columns. We then attempted a logistic regression with sklearn, but could not reach the desired accuracy. After that, we used a tensorflow neural network. Our final model had 2 hidden layers, a 120 neuron sigmoid one, and a 600 neuron relu one. The output layer was sigmoid as well. We ran it for 20 epochs.

## Results
The final predictive model scored an accuracy of 75% on the testing data. 

Code used to generate performance metrics:
https://datascience.stackexchange.com/questions/45165/how-to-get-accuracy-f1-precision-and-recall-for-a-keras-model

## About the files 
The notebook used to get the final model was the Cl_Diabetes_Colab_75.ipynb. In it, we have 3 models that all reach 75%. We also exported images of the setups and results in the results folder. 

The main csv we used was diabetes_binary_5050split_health_indicators_BRFSS2021.csv. This is a pre-balanced version of the data provided by the original uploaders. It makes it so each class has equal numbers of entries.

Converting to sqlite involved using the sqlite_conversion.ipynb.

There is also the diabetes_database.sqlite file, which is the sqlite database we linked to. Of note, if running in colab, this should be uploaded to the temporary folder and it should work with the notebook as is. Otherwise you'll have to change the relevant paths.

Finally, there model_versions.csv. This stores our previous model attempts as well as relevant information about them.
