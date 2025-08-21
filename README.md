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
5.Form the equation of the line:


<img width="176" height="34" alt="image" src="https://github.com/user-attachments/assets/790fda21-f647-4e8c-92cd-3aa0bcc41336" />

   
6.Plot the scatter plot of the given data points and draw the regression line.


## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Rithika R
RegisterNumber:212224240136
*/
import numpy as np
import matplotlib.pyplot as plt

# Step 1: Input data
X = np.array([1, 2, 3, 4, 5])  # Independent variable
Y = np.array([2, 4, 5, 4, 5])  # Dependent variable

# Step 2: Calculate means
X_mean = np.mean(X)
Y_mean = np.mean(Y)

# Step 3: Calculate slope (m)
numerator = np.sum((X - X_mean) * (Y - Y_mean))
denominator = np.sum((X - X_mean) ** 2)
m = numerator / denominator

# Step 4: Calculate intercept (b)
b = Y_mean - m * X_mean

print("Slope (m):", m)
print("Intercept (b):", b)

# Step 5: Regression line
Y_pred = m * X + b

# Step 6: Plotting
plt.scatter(X, Y, color="blue", label="Data Points")
plt.plot(X, Y_pred, color="red", label=f"Y = {m:.2f}X + {b:.2f}")
plt.xlabel("X")
plt.ylabel("Y")
plt.title("Univariate Linear Regression")
plt.legend()
plt.show()

```

## Output:
![best fit line](sam.png)
```
Slope (m): 0.6

Intercept (b): 2.2

Equation of line: Y=0.6X+2.2
```
## Graph:

Blue points → Original data

Red line → Best fit regression line


<img width="721" height="512" alt="image" src="https://github.com/user-attachments/assets/752e072f-d2fa-4b5a-921f-cd35d71f6333" />




## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
