# Milk Quality Improvement (DMAIC + SPC + Decision Tree)

A quality improvement project that analyzes milk production quality using SPC and process capability, and builds a Decision Tree model to predict milk grade for decision support.

## Problem
Milk quality indicators vary across samples, which may cause unstable production outcomes and inconsistent grading. The project aims to detect instability, evaluate capability against specs, and support quality decisions using analytics.

## Objectives
- Identify critical quality factors (CTQ)
- Monitor process stability using SPC (X-bar/R chart)
- Evaluate process capability (Cp, Cpk)
- Build a Decision Tree model to classify/predict milk Grade
- Propose improvement actions and control plan

## Dataset
- File: `milknew.csv`
- Features: pH, Temperature, Colour, Taste, Odor, Fat, Turbidity, ...
- Target: Grade (e.g., A/B/C or Pass/Fail)

## Methods
1. Data cleaning & preprocessing (missing values, encoding, basic checks)
2. Exploratory analysis (relationships among quality variables)
3. SPC monitoring (X-bar/R chart)
4. Process capability analysis (Cp/Cpk)
5. Decision Tree training and evaluation
6. Improvement recommendations + Control plan (DMAIC)

## Tools
Python (Pandas, NumPy, Scikit-learn, Matplotlib), Jupyter Notebook, SPC, DMAIC, Cp/Cpk

## Key Results
- **Process stability:** **Out-of-control** based on X-bar/R charts. Subgroup means frequently exceed the **Upper Control Limit (UCL)**, indicating high instability and **special-cause variation** in pasteurization temperatures.
- **Capability:** **Cp = 0.066**, **Cpk = -0.073**. Process variation is far wider than the allowable tolerance, and the process mean lies **outside the specification limits** (biased above **USL**).
- **Model performance:** **Accuracy = 99.06%**, **F1-score = 0.9906 (Weighted Average)**. The model correctly classified **210/212** test samples with near-perfect performance for the **Medium-quality** class.
- **Key drivers:** **pH** (Primary Splitter/Root Node), **Temperature** (Secondary major split), and **Odor/Fat/Turbidity** (Key sensory refiners).

## Business Impact
- Enables early detection of process drift to reduce defective batches
- Provides quantitative evidence (Cp/Cpk) for customer/spec compliance
- Supports consistent grading decisions using a predictive model

## Repository Structure
- `Milk Project (clean version).ipynb` – Final notebook  
- `milknew.csv` – Dataset  
- `SCLM_449_FINAL_PROJECT_....pdf` – Report  
- `SCLM 449 Milk Company Quality Presentation...` – Slides  

## How to Run
1. Open `Milk Project (clean version).ipynb`
2. Install required libraries:
   - Pandas
   - NumPy
   - Scikit-learn
   - Matplotlib
3. Run all cells

## Author
Huynh Thuy Bao Tram – SCLM449 (Process Control & Improvement)

