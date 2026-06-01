# sEMG Analysis of Ankle Joint Movements in Stroke Patients

## Overview
This project analyzes surface electromyography (sEMG) signals to classify ankle joint movements in healthy individuals and stroke patients. The system extracts 25 time-domain and frequency-domain features from muscle activity recorded from Tibialis Anterior and Gastrocnemius muscles during four ankle movements: dorsiflexion, plantarflexion, eversion, and inversion.

## Purpose
Traditional stroke rehabilitation assessment lacks objective, quantifiable feedback. This project demonstrates that sEMG combined with machine learning can objectively differentiate ankle movement patterns, providing a potential tool for rehabilitation assessment.

## Key Results
- Ensemble Classifier (Bagged Trees) achieved **78.4%** classification accuracy on combined data
- Healthy subjects: **81.3%** accuracy
- Stroke patients: **77.2%** accuracy
- Significant differences (p < 0.05) found in MAV, RMS, and WL features between movement classes and subject groups

## Dataset
- **Participants**: 12 (6 healthy, 6 stroke patients)
- **Movements**: Dorsiflexion, Plantarflexion, Eversion, Inversion
- **Muscles**: Tibialis Anterior (TA), Gastrocnemius (GA)
- **Sampling Rate**: 512 Hz
- **Movement Duration**: 5 seconds with 3 repetitions each

## Features Extracted (25 features per window)

### Time-Domain (18 features)
- Mean Absolute Value (MAV)
- Root Mean Square (RMS)
- Waveform Length (WL)
- Zero Crossing Rate (ZCR)
- Slope Sign Changes (SSC)
- Willison Amplitude (WAMP)
- Variance, Standard Deviation
- Maximum Absolute Value, Peak-to-Peak
- Signal Energy, Signal Power
- Skewness, Kurtosis, Form Factor
- Hjorth Activity, Mobility, Complexity

### Frequency-Domain (7 features)
- Mean Frequency
- Median Frequency
- Peak Frequency
- Total Power
- Spectral Entropy
- Spectral Centroid
- Power Bandwidth

## Classifiers Tested
| Classifier | Accuracy |
|------------|----------|
| Ensemble (Bagged Trees) | 78.4% |
| K-Nearest Neighbors (KNN) | 73.1% |
| Support Vector Machine (SVM) | 71.2% |


