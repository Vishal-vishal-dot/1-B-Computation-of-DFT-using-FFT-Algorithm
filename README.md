# EXPT 1b: Computation-of-DFT-using-FFT-ALGORITHM

## AIM
To perform and verify DFT using FFT-ALGORITHM by SCILAB.
## APPARATUS REQUIRED
PC installed with SCILAB
## PROGRAM 
### DFT FFT-ALGORITHM
```
clear;
clc;
close all;
xn = [1 2 3 4 4 3 2 1];
n1 = 0:1:length(xn)-1;
subplot(2,2,1);
plot2d3(n1, xn);
xlabel('Time n');
ylabel('Amplitude');
title('Input Sequence');
Xk = fft(xn);
K1 = 0:1:length(Xk)-1;
magnitude = abs(Xk);
subplot(2,2,2);
plot2d3(K1, magnitude);
xlabel('Frequency (Hz)');
ylabel('Magnitude (gain)');
title('Magnitude Spectrum');
angle = atan2(imag(Xk), real(Xk));
subplot(2,2,3);
plot2d3(K1, angle);
xlabel('Frequency (Hz)');
ylabel('Phase');
title('Phase Spectrum');
y = ifft(Xk);
n2 = 0:1:length(y)-1;
subplot(2,2,4);
plot2d3(n2, y);
xlabel('Time n');
ylabel('Amplitude');
title('Inverse FFT of X(k)');
```
### CALCULATIONS:
![FFT-1](https://github.com/user-attachments/assets/34a57899-397d-4ec3-8469-189400126edf)

![FFT-2](https://github.com/user-attachments/assets/8712a5e3-c615-4cc1-a2dc-a3f9686c8eea)

### SAMPLE OUTPUT:
<img width="876" height="697" alt="DFT using FFT" src="https://github.com/user-attachments/assets/79c7d5f1-7c8b-4090-bf88-1d75724fd0f1" />

## RESULT:
Thus,  DFT using FFT-ALGORITHM for two given sequences were performed and its result was verified.
