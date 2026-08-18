# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: HEMAVARSHINI D 
RegisterNumber:  212225220039
*/

import numpy as np
import matplotlib.pyplot as plt


X = np.array([1, 2, 3, 4, 5])
Y = np.array([2, 4, 5, 4, 5])


X_mean = np.mean(X)
Y_mean = np.mean(Y)


numerator = np.sum((X - X_mean) * (Y - Y_mean))
denominator = np.sum((X - X_mean) ** 2)
m = numerator / denominator


b = Y_mean - m * X_mean


Y_pred = m * X + b

print(f"Slope (m) = {m:.2f}")
print(f"Intercept (b) = {b:.2f}")
print(f"Regression Equation: Y = {m:.2f}X + {b:.2f}")


plt.scatter(X, Y, color='blue', label='Actual Data')
plt.plot(X, Y_pred, color='red', label='Best Fit Line')
plt.xlabel('X')
plt.ylabel('Y')
plt.title('Univariate Linear Regression using Least Squares')
plt.legend()
plt.grid(True)
plt.show()
```

## Output:
<img width="682" height="574" alt="Screenshot 2026-08-08 141757" src="https://github.com/user-attachments/assets/758e614f-0d9b-4db0-b227-5682889057ae" />



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
