# ECG signal processing

An electrocardiogram (ECG) records the electrical activity of the heart through electrodes on the skin.

## Waveform
- P wave: atrial depolarisation
- QRS complex: ventricular depolarisation (normally under 120 ms)
- T wave: ventricular repolarisation

## Typical noise sources
- Baseline wander (below 0.5 Hz): breathing and body movement
- Powerline interference: 50 Hz in Europe
- Muscle noise (EMG): broadband, overlaps with the QRS frequency range

## Filtering
- High-pass at about 0.5 Hz removes baseline wander
- Notch filter at 50 Hz removes powerline interference
- Low-pass at about 40 Hz reduces muscle noise in monitoring applications
- Zero-phase filtering avoids distorting the ST segment

## R-peak detection (Pan-Tompkins)
Band-pass filter, derivative, squaring, moving-window integration and adaptive thresholds.

## Heart rate variability
- Computed from the RR intervals between consecutive R peaks
- SDNN: standard deviation of the RR intervals
- RMSSD: root mean square of successive RR differences, reflects short-term variability
