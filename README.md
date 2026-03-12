# DSBSC


EX NO: 2	DSB-SC-AM MODULATOR AND DEMODULATOR

AIM:

To write a program to perform DSBSC modulation and demodulation using SCI LAB and study its spectral characteristics

EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	SCI LAB

Note: Keep all the switch faults in off position

Algorithm:

1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the message signal.
•	Amplitude: Maximum amplitude of the message signal.
2.	Generate Signals:
•	Message Signal: A sinusoidal signal that will be modulated.
•	Carrier Signal: A high-frequency sinusoidal signal used for modulation.
3.	DSBSC Modulation:
•	Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
4.	DSBSC Demodulation:
•	Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components).
•	Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
5.	Visualization:
Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation.
PROCEDURE

•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
 
•	Execute the code
•	If any Error, correct it in code and execute again
•	Verify the generated waveform using Tabulation and Model Waveform

Model Waveform

<img width="703" height="679" alt="image" src="https://github.com/user-attachments/assets/e7c7c7f8-ccf2-41ac-b1f3-325989941a6f" />

Program
```
Am=5.8;
Fm=208;
Ac=11.6;
Fc=2080;
Fs=20800;
t=0:1/Fs:2/Fm;
em=am * cos(2 * 3.14 * fm* t);
subplot(3,1,1);
plot(t,em);
ac=14.4;
fc=2440;
ec=ac * cos(2 * 3.14 * fc * t);
subplot(3,1,2);
plot(t,ec);
eam1=ac*(1+(em/ac)). * cos(2 * 3.14* fc * t);
eam2=ac*(-1+(em/ac)). * cos(2 * 3.14* fc * t);
edsbsc=eam1+eam2;
subplot(3,1,3);
plot(t,edsbsc);
```
Output Graph
<img width="1917" height="1198" alt="image" src="https://github.com/user-attachments/assets/b980841a-fbf1-4d72-8a53-a5e20e10da47" />


Tablular Column
![WhatsApp Image 2026-03-12 at 10 10 03](https://github.com/user-attachments/assets/81a310e0-7e02-41fe-80c6-d7f152dacd49)


Result

Thus the DSB-SC-AM Modulation and Demodulation is generated.

