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
Developed by: Divya S
RegisterNumber:212221040042

import numpy as np
import matplotlib.pyplot as plt

# Get input from the user for data points
num_points = int(input("Enter the number of data points: "))
x = np.zeros(num_points)
y = np.zeros(num_points)
for i in range(num_points):
    x[i] = float(input(f"Enter x[{i}]: "))
    y[i] = float(input(f"Enter y[{i}]: "))

# Calculate the mean of x and y
x_mean = np.mean(x)
y_mean = np.mean(y)

# Calculate the slope (m) and y-intercept (b)
numerator = np.sum((x - x_mean) * (y - y_mean))
denominator = np.sum((x - x_mean)**2)
slope_m = numerator / denominator
intercept_b = y_mean - slope_m * x_mean

# Predicted values
y_pred = slope_m * x + intercept_b

# Plot the original data and the regression line
plt.scatter(x, y, label='Original Data')
plt.plot(x, y_pred, color='red', label='Regression Line')
plt.xlabel('X')
plt.ylabel('Y')
plt.title('Univariate Linear Regression')
plt.legend()
plt.show()

print(f"Slope (m): {slope_m}")
print(f"Intercept (b): {intercept_b}")


*/
```

## Output:
![image](https://github.com/divz2711/Univariate-Linear-Regression-to-fit-a-straight-line-using-least-squares/assets/121245222/af09adb1-05ef-4014-b9e6-4900ed37dce0)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
