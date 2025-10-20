# DSBSC-using-python
EX NO:DETECTION AND GENERATION OF DSBSC-AM USING PYTHON

AIM:
To write a program to perform DSBSC modulation and demodulation using COLAB and study its spectral characteristics

EQUIPMENTS REQUIRED

• Computer with i3 Processor

• COLAB

Algorithm:

Define Parameters: • Fs: Sampling frequency. • T: Duration of the signal. • Fc: Carrier frequency. • Fm: Frequency of the message signal. • Amplitude: Maximum amplitude of the message signal.
Generate Signals: • Message Signal: A sinusoidal signal that will be modulated. • Carrier Signal: A high-frequency sinusoidal signal used for modulation.
DSBSC Modulation: • Modulated Signal: Multiply the message signal by the carrier signal to produce the DSBSC signal.
DSBSC Demodulation: • Multiplication: Multiply the modulated signal by the carrier signal to get the product of the message signal with itself (i.e., the original message signal plus high-frequency components). • Low-pass Filtering: Apply a Butterworth low-pass filter to remove the high- frequency components and recover the original message signal.
Visualization: Plot the message signal, carrier signal, DSBSC modulated signal, and the recovered signal after demodulation

MODEL WAVEFORM:

<img width="600" height="500" alt="image" src="https://github.com/user-attachments/assets/5fdbcaca-7004-470b-bd44-08debac90f52" />

PROGRAM:
```
import numpy as np
import matplotlib.pyplot as plt
Am=2.19
fm=284
fs=28400
Ac=3.19
fc=2840
t=np.arange(0,2/fm,1/fs)
m=Am*np.cos(2*3.14*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)
c=Ac*np.cos(2*3.14*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)
s1=(Ac+m)*np.cos(2*3.14*fc*t)
s2=(Ac-m)*np.cos(2*3.14*fc*t)
s=s1-s2
plt.subplot(3,1,3)
plt.plot(t,s)
plt.tight_layout()
plt.show()
```
OUTPUT GRAPH:

<img width="750" height="500" alt="image" src="https://github.com/user-attachments/assets/ab9e5702-3d8c-42bb-b543-93c7bbc1e690" />

TABULATION:

<img width="900" height="1200" alt="image" src="https://github.com/user-attachments/assets/4eb9139c-d9cd-4190-9d2f-0d3aeeac6924" />

RESULT:
Thus the DSB-SC-AM Modulation and Demodulation is generated using python.





