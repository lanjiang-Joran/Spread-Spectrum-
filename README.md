# Spread Spectrum(Study Notes)!
# 1.Spread Spectrum
Spread Spectrum (SS) communication is referred to as spread spectrum communication, which refers to a transmission mode in which the signal bandwidth used to transmit information is much larger than the bandwidth of the information itself. In the spread spectrum communication system, the information source data to be transmitted is first modulated with a set of pseudo-random sequence, that is, PN sequence, and then transmitted after spreading the spectrum, and the same spread spectrum sequence is generated locally at the receiving end for de-expanding and other related processing to recover the data.

Because there's Shannon's formula:
$$C=Blb(1+\frac{S}{N})$$
Where, C is the channel capacity, B is the channel bandwidth, and S/N is the channel output signal-to-noise ratio. When the bandwidth is larger, if the same channel capacity is needed, the required signal-to-noise ratio can be smaller, that is, the signal bandwidth B and the signal-to-noise ratio S/N can be exchanged. Therefore, spread spectrum communication can make the useful signal submerged in the noise under the condition of high bandwidth. In military communication, there is a high requirement for the concealment of useful signals, and the spread spectrum communication, which uses bandwidth to exchange the advantage of SNR, is widely used in military field.
# 2.Spread spectrum technology classification 
## 2.1 Direct sequence spread spectrum
Direct sequence spread spectrum refers to the mode 2 plus (or waveform multiplication) processing of the signal to be transmitted and a Gaussian spread spectrum code to directly expand the signal transmission bandwidth to achieve spectrum expansion technology, the specific principle of the "MATLAB based Communication System simulation" or other books. There are several basic questions in the learning process:

 - Why does spread spectrum use PN code?
1. In PN code, the number of "0" and "1" is basically equal, which has good **randomness**.
2. PN code has good **autocorrelation characteristics** to ensure that the spread spectrum signal is demoded by pseudo random sequence.
3. Different PN codes have very **small cross-correlation characteristics**, which prevents the signals of different PN sequences from interfering with each other after spread spectrum.
4. PN series **total amount is large**, to meet the needs of multiple users.

Among them, autocorrelation is a measure of the correlation degree of the signal, which can be regarded as the integration operation after the multiplication of the time signal and its own delay signal. The autocorrelation characteristics of each PN code are sharp, and the autocorrelation function in the time series data has a significant peak or wave peak at a certain lag order (that is, the autocorrelation function of each spread spectrum sequence should be an impulse function, 0 everywhere except for zero time delay).
A cross correlation is a covariance (sliding dot product) between two vectors X and Y, a digital signal cross correlation function:
$$\rho(\frac{x}{y})=(A-D)$$
## 2.2 Frequency hopping

In frequency modulation communication, the available channel bandwidth is divided into a large number of non-overlapping frequency gaps, and the carrier frequency of traditional narrowband modulated signals is discretized in these frequency gaps in different time intervals under the control of pseudo-random sequences to realize the spectrum expansion of the system. With its excellent anti-interference performance and multi-access networking capability, FM communication technology can be widely used in military wireless anti-interference communication, civil mobile communication, modern radar and sonar electronic systems. See "Communication System Simulation Based on MATLAB" or other books for specific principles.


