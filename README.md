# PHOENIX Spectral Classification Pipeline

## Project Objective
This repository contains a scalable computational astrophysics pipeline designed to automate the classification of stellar metallicities ([Fe/H]) using high-resolution synthetic spectra from the PHOENIX library. The project demonstrates the application of dimensionality reduction and probabilistic machine learning to extract core atomic absorption signatures.

## Pipeline Architecture
1. **Data Acquisition:** Programmatic mining of a 100-star grid ($4000\,\text{K} \le T_{\text{eff}} \le 8500\,\text{K}$ and $-3.0 \le \text{[Fe/H]} \le +1.5$).
2. **Preprocessing:** Visible-light wavelength masking (4000Å - 7000Å) to isolate iron absorption lines, followed by downsampling for computational efficiency.
3. **Dimensionality Reduction:** Principal Component Analysis (PCA) to compress the massive spectral flux vectors into 10 principal components.
4. **Classification:** A Gaussian Naive Bayes algorithm to map mathematical features to physical metallicity classes using Bayesian probability.

## Results
The scaled 100-star model successfully maps spectral features to their respective metallicity classes. As detailed in the attached `stellar_report.pdf`, the resulting confusion matrix displays a strong diagonal trend, with prediction variances restricted strictly to physically adjacent metallicity categories.

## Repository Contents
* `PHOENIX_Spectral_Pipeline.ipynb`: The core Google Colab execution environment.
* `phoenix_ml_dataset_100.csv`: The scaled spectral matrix.
* `confusion_matrix.png`: Visual validation of the Bayesian classifier.
* `stellar_report.pdf`: The formal LaTeX project manuscript.
