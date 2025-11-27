# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Input the augmented matrix of the equations.
2. Use row operations to convert it into upper triangular form.
3. Apply back substitution to find the values of variables.
4. Print the solutions of all variables.

## Program:
```
Program to find the solution of a matrix using Gaussian Elimination.
Developed by:VIJIYALAKSHMI A 
RegisterNumber: 25017569

```
```
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit("Devide by zero detected!")
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end=' ')
```
## Output:

<img width="1231" height="542" alt="Screenshot 2025-11-27 114434" src="https://github.com/user-attachments/assets/6f2f9e2f-333a-45c8-8ee7-199f2b5327b6" />
<img width="1187" height="668" alt="Screenshot 2025-11-27 114451" src="https://github.com/user-attachments/assets/79d22c02-e680-40ad-9553-fe3d00e780a7" />
<img width="1238" height="485" alt="Screenshot 2025-11-27 114507" src="https://github.com/user-attachments/assets/c06b1d58-f731-424c-8065-f092c4776d08" />

## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

