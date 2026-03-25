# Digital-Signal-Processing--Correlation
## AIM:
To generate discrete auto correlation and cross correlation of signals using MATLAB.
## APPARATUS REQUIRED:
MATLAB R2023a.
## ALGORITHM:
Step 1: Open matlab. Write the program.

Step 2: Read the input sequence 1 and input sequence 2 sequence.

Step 3: Perform auto correlation and cross correlation for both the sequences. 

Step 4: Plot the output sequence with x-label and y-label with suitable title.

Step 5: Terminate the program.


## PROGRAM: 

~~~
clc;
clear all;
close all;
% INPUT SIGNAL-1
a = input('enter the starting x(n): ');
x = input('Enter the x(n) sequence: ');
n = a : 1 : length(x) + a - 1;
figure(1)
stem(n, x)
xlabel('Time')
ylabel('Amplitude')
title('Input Signal-1')
% INPUT SIGNAL-2
b = input('enter the starting y(n): ');
y = input('Enter the y(n) sequence: ');
m = input('enter the ending y(n): ');
n1 = b : 1 : length(y) + b - 1;
figure(2)
stem(n1, y)
xlabel('Time')
ylabel('Amplitude')
title('Input Signal-2')
% DISCRETE AUTO CORRELATED SIGNAL
out1 = xcorr(x, x);
n2 = a - m : 1 : length(out1) + a - m - 1;
figure(3)
stem(n2, out1)
xlabel('Time')
ylabel('Amplitude')
title('Discrete auto correlated waveform')
% DISCRETE CROSS CORRELATED SIGNAL
Out2 = xcorr(x,y);
n3 = a - m : 1 : length(Out2) + a - m - 1;
Out2_trimmed = Out2(3:end);    
n3_trimmed = n3(3:end);        
figure(4)
stem(n3_trimmed, Out2_trimmed)
xlabel('Time')
ylabel('Amplitude')
title('Discrete cross correlated waveform (trimmed)')

~~~
## OUTPUT:
## Input Signal-1

<img width="1598" height="853" alt="Screenshot 2026-03-25 190826" src="https://github.com/user-attachments/assets/c3296916-738c-4c44-b8d7-77cc8cf65297" />

## Input Signal-2

<img width="1665" height="867" alt="Screenshot 2026-03-25 190752" src="https://github.com/user-attachments/assets/c5f05e83-75a0-461c-9d91-0e9da573c51b" />

## Discrete auto correlated waveform 

<img width="1644" height="863" alt="Screenshot 2026-03-25 190711" src="https://github.com/user-attachments/assets/b9a65780-7154-470e-a7d9-370ff822a254" />


## Discrete cross correlated waveform (trimmed)

<img width="1660" height="871" alt="Screenshot 2026-03-25 190627" src="https://github.com/user-attachments/assets/38712ba9-7a82-462e-b388-a1583f751270" />

## RESULT:

The cross correlation of x1[n] and x2[n] is {4.6,14.45,9.21,9.49,13.83,10.66,30.89,-19.18,0.55,27.05,**-6.5**,-8.7}
