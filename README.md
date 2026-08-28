# Description

Mechanical validation study comparing torque values from a Con-Trex isokinetic 
dynamometer (IKD) against inverse dynamics (ID) calculations, using a custom 
actuator–force plate setup. 
Developed during my research work at the HUS Motion 
Laboratory, New Children's Hospital, Helsinki.

---

## Repository Contents

- `IKD_ID_Torques_Validation.mlx` — MATLAB Live Script for data processing and analysis:
  - Signal resampling and temporal alignment (IKD vs. ID)
  - Peak torque extraction and Torque Comparison IKD vs IDx/IDy/IDz
- `IKD_ID_Torques_Validation.html` — Rendered output (code, results, plots)

## Analysis Overview

For each trial, the script:
1. Loads raw force plate and lever-arm data, computes ID torque as the product 
   of vertical force and lever-arm length
2. Loads and resamples the corresponding Con-Trex dynamometer data to match the 
   ID sampling rate (100 Hz)
3. Time-aligns the two signals (accounting for trial-specific offsets)
4. Identifies peak torques in both signals and computes the percentage 
   difference relative to the dynamometer reference


## How to Run

1. Download or clone this repository.
2. Open `IKD_ID_Torques_Validation.mlx` in MATLAB.
3. Load the required workspace files:
   - `IKD_Torque_Data.mat` — dynamometer (IKD) torque values
   - `Force_LeverArm_Trials1-4.mat` — force and lever-arm data for trials 1–4
   - `Force_LeverArm_Trials5-8.mat` — force and lever-arm data for trials 5–8
4. Run the script section by section (organized by trial/condition).

Alternatively, open `IKD_ID_Torques_Validation.pdf` to view the rendered output without 
running MATLAB.

## Reference

This work is part of a study submitted to the Journal of Biomechanics and currently under review.
