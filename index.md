**Palm NIRS for Non‑Invasive Glucose Estimation **

**Abstract**
Non-invasive blood glucose monitoring remains a critical challenge in biomedical engineering due to the complex interplay of optical, physiological, and biochemical variables. This study investigates the feasibility of palm-based near-infrared spectroscopy (NIRS) for non-invasive glucose estimation, employing a tiered experimental design that enables a systematic evaluation of how optical interference, scattering, and tissue heterogeneity affect signal quality and model robustness across increasingly realistic biological contexts. While the absorption spectrum of glucose shows strong linearity in controlled solutions, glucose-specific signal characteristics decline in blood and further in palm-based settings. This highlights not only the difficulty of isolating glucose signals in complex, scattering tissues but also the limitations of directly applying idealized optical domain knowledge without accounting for individual variability in tissue composition and palm-specific spectral signatures. To address this, we employ two modeling strategies: a physics-informed approach utilizing Beer–Lambert regularization, and a calibration-augmented approach that incorporates participant-specific tissue optical characteristics. Calibration-augmented model outperforms physics-informed model, achieving an R² of 0.70 and MAE of 25 mg/dL, with all predictions falling within clinically acceptable error zones. These findings underscore the importance of personalized modeling in biologically complex environments and demonstrate that embedding individual-specific optical responses into model representation is critical for accurate non-invasive glucose estimation using NIRS.

Repository structure
data/: raw and processed spectral datasets (CSV/Parquet)
code/: notebooks and scripts for preprocessing, modeling, and evaluation
docs/: figures and supplementary documentation (if using /docs as Pages source, put this file here)
models/: saved model artifacts and calibration parameters
licenses/: data/code licenses and third‑party notices

**Download data**
Calibration spectra (phantoms/solutions): data/phantom_spectra.csv

Whole blood spectra: data/blood_spectra.csv

Palm NIRS spectra: data/palm_spectra.csv

Reference glucose values: data/reference_glucose.csv

Train/validation splits: data/splits.json

**Code and reproduction** 
Preprocessing pipeline: code/preprocess.ipynb

Physics‑informed baseline (Beer–Lambert regularization): code/physics_informed.ipynb

Calibration‑augmented model: code/calibration_augmented.ipynb

Evaluation and figures: code/evaluate.ipynb

**Key results**
Calibration‑augmented model: R² = 0.70, MAE = 25 mg/dL on palm datasets

All predictions fall within clinically acceptable error zones

Glucose‑specific features degrade from solutions → blood → palm tissues, emphasizing tissue scattering and heterogeneity impacts

**How to cite**
If you use this dataset or code, please cite:

“Palm‑based Near‑Infrared Spectroscopy for Non‑Invasive Glucose Estimation: Tiered Validation and Calibration‑Augmented Modeling,” Authors, Year, DOI/URL.

**License**
Data license: CC BY 4.0 (or specify)

Code license: MIT (or specify)

Contact
For questions and collaboration: your.email@domain
