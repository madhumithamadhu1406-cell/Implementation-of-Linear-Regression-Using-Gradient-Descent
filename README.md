# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Initialize parameters (slope and intercept) with small values and choose a learning rate.
2. Compute predicted profit using the linear equation for all training data points.
3. Calculate the cost (error) and update parameters using gradient descent to minimize the error.
4. Repeat the process until convergence and use the final model to predict profit.

## Program:
```
Program to implement the linear regression using gradient descent.
Developed by: Madhumitha V
RegisterNumber:212225040218
import numpy as np
import matplotlib.pyplot as plt
X = np.array([1, 2, 3, 4, 5], dtype=float)
y = np.array([2, 4, 5, 4, 5], dtype=float)
m = 0  # slope
b = 0  # intercept
learning_rate = 0.01
epochs = 1000
n = len(X)
for i in range(epochs):
    y_pred = m * X + b
    dm = (-2/n) * np.sum(X * (y - y_pred))
    db = (-2/n) * np.sum(y - y_pred)
    m = m - learning_rate * dm
    b = b - learning_rate * db
print("Slope (m):", m)
print("Intercept (b):", b)
y_pred = m * X + b
plt.scatter(X, y, color='blue', label='Actual Data')
plt.plot(X, y_pred, color='red', label='Regression Line')
plt.xlabel("X")
plt.ylabel("y")
plt.legend()
plt.show()

```


## Output:
<img width="1236" height="729" alt="Screenshot 2026-04-29 114230" src="https://github.com/user-attachments/assets/5dddb83b-66c9-4755-869c-437c993b0367" />



## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
