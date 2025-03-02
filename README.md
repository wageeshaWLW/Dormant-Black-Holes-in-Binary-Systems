# Dormant Black Holes in Binary Systems  

## Introduction  

This project explores the presence of dormant black holes (BHs) in binary systems using **Gaia Data Release 3 (DR3)**. With advancements in gravitational wave astronomy and high-precision astrometry, the detection of compact objects in massive binary systems has gained significant importance. These binaries are essential for understanding the evolution leading to compact object mergers.  

The focus is on binary systems where a **black hole coexists with a Main Sequence (MS) star**. Due to the difficulty of direct observation, the study relies on computational simulations to analyze the evolution of such systems and compare synthetic models with observed candidates.  

## Methodology  

To simulate binary system evolution, the project utilizes **Binary System Evolution (BSE)** via **SEVN (Stellar EVolution for N-body)**. SEVN evolves binaries based on initial parameters, such as:  

- **Masses**  
- **Spin**  
- **Semi-major axis**  
- **Orbital eccentricity**  

Stellar evolution is determined by interpolating **pre-computed stellar tracks**, while binary interactions are modeled using **analytic and semi-analytic approaches**. SEVN’s modular design allows easy integration of different stellar evolution models without modifying the underlying code structure.  

Additionally, **Machine Learning techniques** such as **Deep Neural Networks (DNN) and XGBoost** are employed to classify and interpret the properties of potential black hole candidates. The project also attempts to reconstruct the evolutionary history of observed candidates by matching them with simulated systems.  

## Objectives and Analysis  

- **Identification and classification** of BH+MS binary systems from Gaia DR3.  
- **Comparison of real and synthetic populations** to determine the likelihood of observed candidates following specific evolutionary paths.  
- **Feature importance analysis** to evaluate key factors influencing binary evolution.  
- **Development of a similarity metric** to quantify how closely simulated systems match observed candidates.  

## Project Components  

### 🔍 **Data Processing and Analysis**  

- 📂 `bse_bhms_classification.ipynb` – Main notebook for classification and analysis.  
- 📂 `bse_bhms_predict_history.ipynb` – Evaluates system similarity metrics.  
- 📂 `candidates_clean.csv` – Dataset with key features of Gaia BH+MS candidates.  
- 📂 `real_candidates.ipynb` – Generates the candidate dataset.  

### 🏗 **Computational Models**  

- 📄 `sample_df.py` – Python script for generating synthetic samples based on candidate data.  

### 📑 **Documentation and Presentation**  

- 📜 `Projrct_report.pdf` – Detailed project report summarizing findings.  
- 📊 `Project_presentation.pdf` – Presentation slides outlining research and results.  



## SEVN – Binary System Evolution Tool  

**SEVN** is a **C++-based rapid binary population synthesis code** designed for evolving binary systems efficiently. It integrates pre-computed stellar evolution tables and allows real-time selection of different stellar models without modifying the core code. SEVN employs **OpenMP parallelization** for enhanced computational performance, making it ideal for large-scale simulations.  



