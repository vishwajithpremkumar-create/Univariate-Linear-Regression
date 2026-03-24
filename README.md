# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
import numpy as np
import matplotlib.pyplot as plt

X = np.array(list(map(float, input().split())))
Y = np.array(list(map(float, input().split())))

m = np.sum((X - X.mean()) * (Y - Y.mean())) / np.sum((X - X.mean())**2)
c = Y.mean() - m * X.mean()

Y_pred = m * X + c

print(m, c)
print(Y_pred)

plt.scatter(X, Y)
plt.plot(X, Y_pred, 'r')
plt.show()


```
## Output

<img width="1920" height="1080" alt="Screenshot 2026-03-24 101210" src="https://github.com/user-attachments/assets/eebcf1e0-c7ca-43dc-8a89-5700b4b166ff" />


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
