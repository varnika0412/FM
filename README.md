# FM

EXP NO: 4	GENERATION AND DETECTION OF FM


AIM:
To write a program for Frequency Modulation and Demodulation using SCILAB and to observe and measure the frequency deviation and the modulation index of FM.


EQUIPMENTS REQUIRED

•	Computer with i3 Processor
•	SCI LAB

THEORY:

Frequency modulation is a type of modulation in which the frequency of the high frequency (carrier) is varied in accordance with the instantaneous value of the modulating signal.
FREQUENCY DEVIATION f and MODULATION INDEX m f :
The frequency deviation f represents the maximum shift between the  modulatedsignal
frequency, over and under the frequency of the carrier.

We define modulation index m f the ratio between f and the modulating frequency
m= f / fm


FREQUENCY MODULATION GENERATION:
The circuits used to generate a frequency modulation must vary the frequency of a high frequency signal (carrier) as function of the amplitude of a low frequency signal (modulating signal). In practice there are two main methods used to generate FM.
Algorithm
1.	Define Parameters:
•	Fs: Sampling frequency.
•	T: Duration of the signal.
•	Fc: Carrier frequency.
•	Fm: Frequency of the modulating signal.
•	Beta: Modulation index, which controls the extent of frequency deviation.
2.	Generate Signals:
•	Modulating signal: Sinusoidal signal used for modulation.
•	Carrier signal: The high-frequency carrier signal.
•	Modulated signal: FM modulated signal calculated by varying the carrier frequency according to the modulating signal.
3.	FM Modulation:
•	Modulated signal is obtained by modulating the carrier signal with the modulating signal.
 
4.	FM Demodulation:
•	Differentiation: Computes the derivative of the modulated signal to extract frequency variations.
•	Envelope Detection: Takes the absolute value to retrieve the envelope of the signal.
•	Low-pass Filtering: Applies a Butterworth low-pass filter to smooth the envelope and recover the original modulating signal.
5.	Visualization:
•	Plots the modulating signal, carrier signal, FM modulated signal, and demodulated signal for analysis.



PROCEDURE


•	Refer Algorithms and write code for the experiment.
•	Open SCILAB in System
•	Type your code in New Editor
•	Save the file
•	Execute the code
•	If any Error, correct it in code and execute again
Verify the generated waveform using Tabulation and Model Waveform

MODEL GRAPH:

<img width="512" height="365" alt="image" src="https://github.com/user-attachments/assets/acd787bd-5281-4f1b-802f-1aa39fac9189" />


Program
```
Am=4;
fm=333;
fs=33300;
Ac=8;
fc=3330;
t=0:1/fs:2/fm;
B=4.1;
m=Am*cos(2*3.14*fm*t);
subplot(3,1,1);
plot(t,m);
c=Ac*cos(2*3.14*fc*t);
subplot(3,1,2);
plot(t,c);
s=Ac*cos((2*3.14*fc*t)+B*sin(2*3.14*fm*t));
subplot(3,1,3);
plot(t,s);

```


Output Waveform

<img width="1920" height="1140" alt="image" src="https://github.com/user-attachments/assets/52085119-40de-4dad-ae05-923660b9f753" />




Tabulation
![WhatsApp Image 2025-10-08 at 09 55 22_0fadb4d5](https://github.com/user-attachments/assets/3f4daca8-135d-443a-b508-2dd418e3ed4d)




Calculation
![WhatsApp Image 2025-10-08 at 09 55 42_a6f7c4f6](https://github.com/user-attachments/assets/bccdf3dc-1c61-4f6d-97c9-ff7335296083)




Frequency Deviation Practical = 1497.6

Modulation Index Practical	= 4.1

Modulation Index Theoretical	=4.4



RESULT:

Thus, the frequency modulation and demodulation is successfully done and the output is experimentally verified.


