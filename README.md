# EXPT-6-Simulation-of-Multirate-DSP-using-Decimation-and-Interpolation

# AIM: 

# To perform and verify Multirate-DSP-using-Decimation-and-Interpolation.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
```
clc;
clear;
close;
n = 0:%pi/50:2*%pi;
x = sin(%pi*n);   // original signal
M = input("Enter the downsampling factor M = ");
L = input("Enter the upsampling factor L = ");
downsampling_x = x(1:M:length(x));
disp("Input signal x(n) = ");
disp(x);
disp("Downsampled Signal = ");
disp(downsampling_x);
figure(1);
subplot(2,1,1);
plot2d3(1:length(x), x);
xtitle("Original Signal");
subplot(2,1,2);
plot2d3(1:length(downsampling_x), downsampling_x);
xtitle("Downsampled Signal by factor M");
upsampling_x = zeros(1, L*length(x));
for i = 1:length(x)
    upsampling_x(1, L*(i-1)+1) = x(i);
end
disp("Upsampled Signal = ");
disp(upsampling_x);
figure(2);
subplot(2,1,1);
plot2d3(1:length(x), x);
xtitle("Original Signal");

subplot(2,1,2);
plot2d3(1:length(upsampling_x), upsampling_x);
xtitle("Upsampled Signal by factor L");
```
# OUTPUT: 
<img width="757" height="596" alt="Screenshot 2026-09-02 201719" src="https://github.com/user-attachments/assets/b6e6d4c4-33f5-437f-a670-f884d0c2b0a5" />
<img width="760" height="597" alt="Screenshot 2026-09-02 201741" src="https://github.com/user-attachments/assets/863bc2b2-0089-473f-95fb-a5e6bc34deee" />

# RESULT: 
Thus the Multirate-DSP-using-Decimation-and-Interpolation using python was performed and verified.
