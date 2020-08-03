# logistic-regression

lets build a ML model using the library sklearn

#lets import the libraries first

import pandas as pd

import numpy as np

#load the dataset

df=pd.read_csv(r'C:\Users\Sanjana\train.csv')

#your data set is loaded now ,you can check the first five rows using the head function

df.head()

#lets do some data exploration

#to see the shape i.e the number of rows and columns in the data use shape

df.shape

#you can use the describe fuction to see the mean ,median,std dev and other details about your data set.

df.describe()

#now you can find out the null values using null function and futurn fill them or delete them according to your use.

df.isnull().sum() #we are using sum to see the total numbers of null values

#to fill

df.fillna(df.mean,inplace=True)#we use inplace=True to make the changes in the dataset

#to drop or delete

data=df.drop('column_name',axis=1)#we are using axis =1 to provide the information about the location. axis=0 for rows and axis=1 for columns

#let us split the model ,this can be done through sklearn or simply specifying the rows.

#either

train1=df[:500]

test1=df[500:] #this will devide your entire training data set into two parts train and validationset

#or

x=train.drop['column_name',axis=1] #we are dropping the target column and will store in another variable

y=train['column_name']

from sklearn.model_selection import train_test_split

train_x,test_x,train_y,test_y=tarin_test_split(x,y,test_size=0.2)#test_size determines the size of your test file


#lets import the library to carry to build the model

from sklearn.linear_model import LogisticRegression

#make an object as sklearn requires objects to carry out the functions

logreg=LogisticRegression()

#lets fit the model

logreg.fit(train_x,train_y)#train_x is the independent variable while train_y is the target variable

#on performing this you may get some errors whic should be treated accordingly ,make sure you dont have any null values in your data set and strings are converted.

#let us now predict 

pred=logreg.predict(test_x)

pred# check your predictions..

#you can check the accuracy of your model using score function

logreg.score(test_x,test_y)#checking on validation set

#or

logreg.score(train_x,train_y)

#Thankyou!

I am also a beginner any advices are most welcome.
