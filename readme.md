# Typical Radar Jamming Signal Simulation [with MATLAB Code]

1. Distance deception interference simulation in Matlab code
The code simulates the generation process of distance deception interference in radar systems. At the beginning, the program first generates a standard linear frequency modulation (LFM) radar transmission signal with a bandwidth set to 100 MHz, pulse width of 25 microseconds, and a sampling rate of 2.4 GHz. Subsequently, a backscatter signal containing a real target is constructed: by inserting the LFM signal at a certain time point and adding Gaussian noise, the reflected signal received by the radar from the real target is simulated.
Next, the program inserts a delayed and amplified LFM signal into the backscatter signal through setting a deceptive distance (e.g., 50 meters) and calculating the corresponding sampling delay, thus creating a false target response and forming a distance deception interference. The deceptive signal is added to the original backscatter signal to form a composite signal that the radar receives in the interference scenario. Subsequently, a matched filter is used for pulse compression processing on the original backscatter signal, the deceptive signal, and the synthetic signal, comparing their peak response positions and amplitudes to observe the interference effect.
In the dataset generation mode, the program will batch change the deceptive distance (such as 20, 30, 50 meters, etc.) and the interference power ratio (such as 0.8 to 2.0 times), generating multiple samples with synthesised pulse compression results under different parameter combinations. These results along with parameter labels are saved for subsequent interference recognition model training. The entire process supports both visual analysis of individual samples and large-scale training data construction, facilitating research and detection of behavior characteristics of distance deception interference in real systems.
Figure 1: LFM signal
Figure 2: Backscatter signal
Figure 3: Real target pulse compression
Figure 4: Distance deception interference signal
Figure 5: Synthetic signal
Figure 6: Comparison of interference effects
2. Density-Manipulated False Target Interference
This code simulates the process of generating a dataset for density-manipulated false target interference. At the beginning of the simulation, a standard linear frequency modulation (LFM) radar signal is first generated with typical parameters such as a bandwidth of 100 MHz, a pulse width of 25 microseconds, and a sampling rate of 2.4 GHz, and a real target echo signal is constructed by inserting an LFM signal at the middle position and adding Gaussian noise to simulate the reception process of the target echo. Subsequently, pulse compression is performed to analyze the distance characteristics of the target.
In single demonstration mode, the program constructs multiple densely arranged false targets by inserting unit pulses with a scaling factor of 1 at different delay points on the time axis to form sparse pulse columns, which are then convolved with the LFM signal to obtain the interference signal. This interference signal is again convolved with a matched filter to achieve the effect after pulse compression, which can be observed in the figure as multiple pseudo targets appear in the distance dimension, thereby achieving the purpose of interfering with the radar's recognition ability.
In batch mode, the program iterates through different numbers of false targets (e.g., 3 to 6), and the distance between each pair of false targets (e.g., 3 meters to 50 meters), generating multiple random samples for each group of parameters and adding different intensity noise to form a diverse dataset. Finally, each sample includes the pulse-compressed signal, interference parameters, and labels, forming a complete set of training data for density-manipulated false target interference, which can be used for subsequent identification or classification model development. The entire process supports graphic display and large-scale sample generation, balancing analysis and practicality.
Figure 7: LFM Signal
Figure 8: Echo Signal
Figure 9: Pulse Compression
Figure 10: Compressed Signal (Original)
Figure 11: Compressed Signal (Normalized)
3. Smart Noise Jamming Implementation
The program is designed to generate and analyze smart noise jamming, which operates in two modes: "Single-Shot Mode" and "Batch Data Set Mode." In the "Single-Shot Mode," the program simulates an ideal target echo signal and then generates a noisy signal with a blurred shape and controlled power, overlapping with the target echo in time domain to mask the true target position. This noise is shaped by Gaussian envelopes and adjusted in power based on the set dry-to-wet ratio (JSR) to achieve realistic interference effects, ultimately revealing the blurred results after pulse compression.
The entire process relies on multiple parameter configurations, such as radar bandwidth, pulse width, sampling rate, target SNR, JSR (dry-to-wet ratio), and noise width factor (controlling the degree of interference blur). The noise width factor determines the extent to which the interference noise extends relative to the target signal; the higher the value, the more blurred and difficult it is to locate the target.
In the "Batch Data Set Mode," the program iterates over multiple combinations of JSR and noise width, generating multiple samples for each combination and normalizing them through pulse compression before saving them as a dataset. This approach can be used for training models for target recognition or interference recognition. The resulting file, smart_noise_dataset.mat, contains a large number of structured interference samples along with their corresponding parameters, facilitating subsequent analysis and modeling.
Figure 12: LFM Signal
Figure 13: Time-Domain Signal Comparison Analysis
Figure 14: Frequency-Domain Characteristics Analysis
Figure 15: Pulse Compression Results Overview
Figure 16: Detailed Comparison of Smart Noise Jamming Effects

## Images

![Typical radar jamming signal simulation [with MATLAB code]](01.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](02.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](03.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](04.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](05.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](06.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](07.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](08.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](09.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](10.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](11.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](12.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](13.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](14.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](15.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](16.jpg)
![Typical radar jamming signal simulation [with MATLAB code]](17.jpg)

<!-- PAYMENT_BLOCK -->

## Get this dataset

- Payment link (Stripe): [Buy now](https://buy.stripe.com/3cs8yP7sY87d0vu9AB)
- Payment QR code: ![Payment QR code](pay.png)

<!-- /PAYMENT_BLOCK -->
