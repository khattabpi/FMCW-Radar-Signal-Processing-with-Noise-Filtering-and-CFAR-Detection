# FMCW Radar Signal Processing with Noise Filtering and CFAR Detection

This MATLAB project simulates an FMCW (Frequency-Modulated Continuous Wave) radar system, including signal generation, noise addition, filtering, frequency analysis, and CFAR (Constant False Alarm Rate) detection.

## Project Features

- FMCW radar waveform simulation.
- Beat signal generation with Gaussian noise addition.
- Design and application of Butterworth low-pass filter.
- Range FFT and 2D FFT for Range-Doppler Map (RDM) generation.
- SNR computation before and after filtering.
- Visual comparison in time and frequency domains.
- CFAR algorithm applied on the RDM for target detection.

---

##  Structure

- **Signal Generation**
  - Initial position and velocity of target
  - Radar parameters (bandwidth, chirp slope, etc.)
  - Transmitted and received signals computed with time delay

- **Noise Simulation**
  - Gaussian noise added to the beat signal

- **Filtering**
  - Butterworth low-pass filter designed based on desired specifications
  - Applied to noisy beat signal

- **Time and Frequency Domain Analysis**
  - Time-domain comparison: original vs noisy vs filtered signals
  - Frequency-domain (FFT) comparison
  - SNR (Signal-to-Noise Ratio) computation

- **Range and Doppler Estimation**
  - 1D FFT for range estimation
  - 2D FFT for Range-Doppler Map visualization

- **CFAR Detection**
  - Sliding window CFAR applied to 2D RDM
  - Training, guard, and offset parameters defined
  - Threshold computed dynamically per cell
  - Binary detection map output

---

##  Visualization

- ✅ Time-Domain Comparison
- ✅ Frequency-Domain Comparison
- ✅ Magnitude Response of Filter
- ✅ Range FFT
- ✅ Range-Doppler Maps (before and after filtering)
- ✅ CFAR Detection Output (3D surface plot)

---

## Key Parameters

| Parameter               | Value              |
|------------------------|--------------------|
| Carrier Frequency (fc) | 77 GHz             |
| Max Range              | 200 m              |
| Range Resolution       | 1 m                |
| Target Velocity        | -20 m/s            |
| Bandwidth (B)          | `c / (2 * d_res)`  |
| Sampling Frequency     | 8000 Hz            |
| CFAR Training Cells    | Tr = 7, Td = 7     |
| CFAR Guard Cells       | Gr = 3, Gd = 3     |
| CFAR Offset            | 8 dB               |

---

##  Output Metrics

- **SNR before filtering:** Computed from beat signal power and noise power.
- **SNR after filtering:** Computed from filtered signal power and noise power.
- **Noise Floor Reduction:** Clearly visible in frequency plots and Range-Doppler Map after filtering.
- **CFAR Map:** Binary detection map showing targets above dynamic threshold.


## Example Visuals

- **Filtered vs. Unfiltered Beat Signal**
- **Frequency Response of Filter**
- **Before/After Range-Doppler Map**
- **CFAR Output Map**

---

## Requirements

- MATLAB (recommended version: R2021a or newer)
- Signal Processing Toolbox (for `butter`, `freqz`, etc.)


## License

This project is for educational and research use. Feel free to modify and build upon it.
