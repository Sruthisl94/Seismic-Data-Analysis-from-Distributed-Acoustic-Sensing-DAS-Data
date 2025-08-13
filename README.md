# Seismic-Data-Analysis-from-Distributed-Acoustic-Sensing-DAS-Data
## Objective:
Analyze raw seismic DAS data from the Stanford DAS dataset to explore temporal patterns, amplitude variations, and frequency characteristics.

## Description:
This project aims to visualize DAS seismic waveform data stored in SEG-Y format. Extract the key statistics such as amplitude ranges, signal duration, and sampling rate, and use time-domain and frequency-domain plots to understand the seismic activity patterns. The analysis includes waveform visualization, spectrogram generation, and signal filtering to reveal both short-term and long-term variations in the data.
## Goal: 
* Load the seismic waveform data

* Visualize the signal from multiple channels

* Extract basic statistical and frequency-domain features

* Interpret patterns that might correspond to environmental noise, seismic events, or human activity

### Data Source
* File: cbt_processed_20190101_000104.511+0000.sgy

* Sampling: 15,000 samples per channel

* Channels: Multiple fiber optic sensing points

* Type: DAS seismic strain-rate data

### Steps Performed
* Load Data using segyio in Python without geometry interpretation

* Convert seismic traces into a NumPy array for analysis

* Visualize a single channel waveform over time

* Compute basic statistics (mean, max, min, standard deviation)

* Perform Fast Fourier Transform (FFT) to see frequency components

Identify patterns such as:

* High-frequency spikes → local noise or human activity

* Low-frequency waves → possible distant seismic events

## Discussion
The waveform shows short bursts of high amplitude, which could indicate transient events like vehicle movements or construction.

Background noise is relatively constant across most of the time series, suggesting low seismic activity during this period.

Frequency analysis shows dominant low-frequency components with occasional high-frequency spikes, consistent with environmental noise mixed with anthropogenic activity.

Since the DAS system is sensitive to both seismic and vibration sources, interpretation requires context (location, time, and known activities).
