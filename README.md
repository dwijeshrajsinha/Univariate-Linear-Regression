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
DEVELOPED BY: DWIJESH RAJ SINHA Y
REGISTER NO: 212225240038

import numpy as np
import matplotlib.pyplot as plt

#Preprocessing Input data

x=np.array([0,1,2,3,4,5,6,7,8,9])
y=np.array([1,3,2,5,7,8,8,9,10,12])

plt.scatter(x,y)
plt.show()
#Building the model
x_mean=np.mean(x)
y_mean=np.mean(y)

num=0
den=0
for i in range(len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    den+=(x[i]-x_mean)**2
m=num/den
c=y_mean-m*x_mean
print(m,c)
#Making predicitions
y_pred=m*x+c
print(y_pred)

plt.scatter(x,y) #actual
#plt.scatter(x,y_pred,color='red')
plt.plot([min(x),max(x)],[min(y_pred),max(y_pred)],color='red') #predicted
plt.show()
```
## Output
<img width="1056" height="822" alt="image" src="https://github.com/user-attachments/assets/5e96b590-204d-4463-a6c5-3eeaedc98aad" />
<img width="1071" height="664" alt="image" src="https://github.com/user-attachments/assets/eab06250-149e-4d3b-af4a-3c542294046f" />
<img width="914" height="619" alt="image" src="https://github.com/user-attachments/assets/d8ac635e-aa88-477a-a144-b5360643f806" />

## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
