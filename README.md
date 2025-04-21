# EEG-Based Alcoholic vs Non-Alcoholic Classification

## 📖 Overview

Alcohol consumption poses significant health risks, contributing to infectious diseases, cancer, cardiovascular issues, and mental health disorders. Chronic use leads to multisystem damage including immunosuppression, neuropsychiatric effects, and fetal alcohol spectrum disorders.

Many countries (US, UK, Canada, Australia) follow a **Six-Month Rule** — requiring alcoholic patients to remain sober for six months before being considered for a liver transplant. This improves transplant outcomes and ensures optimal use of limited organs.

**Classifying alcoholic and non-alcoholic individuals is crucial before treatment** — to ensure appropriate care, reduce health risks, and improve patient outcomes.

---

## 📊 Dataset Information

-  **Source:** [UCI EEG Database](https://archive.ics.uci.edu/dataset/121/eeg+database)
- EEG signals recorded from **64 scalp electrodes** at **256 Hz** for **1 second per trial**.
- **122 subjects** divided into alcoholic and control groups.
- Each subject completed **120 trials** using images from the *Snodgrass and Vanderwart picture set (1980)*.
- **Stimulus types:**
  - 📷 **Single stimulus (S1)** — one image.
  - 📷 **Matched pair (S1 = S2)** — same image twice.
  - 📷 **Non-matched pair (S1 ≠ S2)** — two different images sequentially.

EEG recordings followed standard electrode placement protocols.

---

##  Frequency Bands in EEG signals

![image](https://github.com/user-attachments/assets/52fd055e-d04e-4ce7-a518-42e7e7bca133)


---

##  Methodology

###  Preprocessing:
- Load raw EEG signals.
- Remove artifacts and normalize signals.

###  Feature Extraction:
- **Wavelet Transform (WT):** Extracts time-frequency localized features.
- **Hilbert-Huang Transform (HHT):** Captures instantaneous frequency-based features ideal for non-linear, non-stationary EEG data.

###  Model Development:
- Building ML Model - Support Vector Machine (SVM)**.
- Train using extracted features.
- Evaluate using metrics: **accuracy**, **ROC-SCORE**.

---

## 🛠 Tech Stack

**Languages:** Python  
**Libraries:** Numpy, Pandas, PyWavelets, Scipy, PyEMD (for HHT), Scikit-learn, Matplotlib, Seaborn  

---

## Conclusion

- EEG signals offer a reliable way to differentiate alcoholic brain activity due to prolonged alcohol-related alterations in brain patterns.
- Combining **Wavelet** and **HHT** improves time-frequency resolution, capturing subtle brainwave variations for classification.

