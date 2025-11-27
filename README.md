# Mean-Variance-And-Cross-Correlation

---

### Aim:

To write a program for mean, variance and cross correlation in SCILAB and verify the output.

---

### Equipments Required:

- Computer with i3 Processor 
- SCI LAB

---

### Algorithm:

1. Define the Function: Specify the function you want to simulate.
   For example,f(x)=sin⁡(x)f(x)=\sin(x)f(x)=sin(x) or any other function.
2. Generate Sample Points: Decide on the range and the number of sample points.
   Generate these sample points within the desired range.
3. Evaluate the Function: Compute the function values at each of these sample points.
4. Compute Mean, Variance and Cross Correlation: Use Scilab's functions to calculate the mean
   and variance of the computed function values.
6. Display Results: Output the computed mean variance and Cross Correlation

---

### Procedure:

1. Refer algorithms and write code for the experiment.
2. Open Scilab in System
3. Type your code in the New Editor
4. Save the file
5. Execute the code
6. If any error, correct it in code and execute again.
7. Verify the generated results.

---

### Program:

```sci
clear; clc; clear;
function X = f(x)
    X = 3 * x .* (1-x).^3;
end
a = 0;
b = 1;
EX = intg(a, b, f);
function Y = c(y)
    Y = 3 * y .* (1-y).^3;
end
EY = intg(a, b, c);
mprintf("i)   Mean of X = %.2f\n     Mean of Y = %.2f\n", EX, EY);
function X = g(x)
    X = x.^2 .* 3 .* (1- x).^3;
end
EX2 = intg(a, b, g);
function Y = h(y)
    Y = y.^2 .* 3 .* (1-y).^3;
end
EY2 = intg(a, b, h);
vX2 = EX2 - (EX)^2;
vY2 = EY2 - (EY)^2;
mprintf("ii)  Variance of X = %.6f\n     Variance of Y = %.6f\n", vX2, vY2);

x= input("type in the reference sequence="); 
y= input("type in the second sequence   =");

n1=max(size(y))-1;
n2=max(size(x))-1;

r=corr(x,y,n1);

clf();
plot2d3(1:length(r), r);

```

---


### Output:


![WhatsApp Image 2025-11-27 at 20 24 18_48affc73](https://github.com/user-attachments/assets/cccb8f7b-1c5b-4856-aed0-de86528c0f1e)

---

### Tabulation:
![WhatsApp Image 2025-11-27 at 19 28 46_cf38e64f](https://github.com/user-attachments/assets/abe8caa3-5e65-4fc3-af53-af296b419bfa)

![WhatsApp Image 2025-11-27 at 19 28 07_c1150278](https://github.com/user-attachments/assets/f3868fa6-7fc6-475d-be5c-6292b13dee42)

---

### Calculation:
![WhatsApp Image 2025-11-27 at 19 27 32_364e1fb3](https://github.com/user-attachments/assets/38de750c-87a7-4106-9641-393e486bd86a)

---

### Result:

Thus the mean, variance and cross correlation are executed in Scilab and the output is verified.
