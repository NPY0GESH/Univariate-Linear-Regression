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

import numpy as np

x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])

plt.scatter(x,y)
plt.show()

xmean = np.mean(x)
ymean = np.mean(y)

num=0
den=0

for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2

m = num/den
b = ymean - m*xmean

print(m,b)
y_pred = m*x+b
print(y_pred)






## Output
</br>
</br>
</br>
</br>
<img width="707" height="544" alt="image" src="https://github.com/user-attachments/assets/dcdb5207-82a0-4b1c-80f6-6094ef727f2c" />
<img width="702" height="523" alt="image" src="https://github.com/user-attachments/assets/5cf35695-827f-4477-9555-f06f5d6a2968" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
