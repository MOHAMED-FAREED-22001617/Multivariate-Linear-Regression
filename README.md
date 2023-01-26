# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
<br>Import Pandas library and linear_model from sklearn using import statement.

### Step2
<br>Read the given csv file using read_csv() method.

### Step3
<br>Create two arrays, independent array x with two classes and dependent array y with one class. Find the regression of x and y using linear_model.LinearRegression() method and fit x and y usind .fit() method.

### Step4
<br>Find the coefficients using .coef_ and intercept using .intercept.

### Step5
<br>Predict the liner regression using regr.predict() method and display the result.

## Program:
```python


import pandas as pd
from sklearn import linear_model
df=pd.read_csv("cars.csv")
x=df[['Weight','Volume']]
y=df['CO2']
regr=linear_model.LinearRegression()
regr.fit(x,y)
print("Coefficient:",regr.coef_)
print("Intercept:",regr.intercept_)
predictedCO2=regr.predict([[3300,1300]])
print("Predict CO@ for the corresponding weight and volume",predictedCO2)



```
## Output:

![Screenshot from 2023-01-25 22-31-19](https://user-images.githubusercontent.com/121412904/214851614-10fa4ab1-ab9a-4929-b5b0-92be02daedf6.png)


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
