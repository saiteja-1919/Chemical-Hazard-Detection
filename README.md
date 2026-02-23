# Chemical Hazard Prediction using Machine Learning

This project is an end-to-end Machine Learning system that predicts whether a chemical compound is Hazardous or Non-Hazardous using molecular structure information derived from SMILES representations.

## Features
- Automated dataset cleaning and preprocessing
- Molecular descriptor extraction using RDKit
- 1024-bit Morgan fingerprint generation
- Missing property retrieval using PubChemPy
- Random Forest and Gradient Boosting model training
- Model evaluation using Accuracy and F1-score
- Confusion matrix visualization
- Interactive Gradio web application for prediction

## Technologies Used
- Python
- Pandas
- NumPy
- RDKit
- PubChemPy
- Scikit-learn
- Matplotlib
- Seaborn
- Gradio
- Joblib

## Methodology
- Load and clean chemical dataset
- Remove invalid SMILES values
- Convert Hazard label (Yes/No → 1/0)
- Extract molecular descriptors:
  - Molecular Weight
  - LogP
  - H-Bond Donors
  - H-Bond Acceptors
  - TPSA
  - Rotatable Bonds
  - Ring Count
  - Heavy Atom Count
- Generate 1024-bit Morgan fingerprints
- Combine descriptors and fingerprints into a feature matrix
- Split dataset into 80% training and 20% testing
- Train Random Forest and Gradient Boosting classifiers
- Evaluate models using Accuracy and F1-score

## Model Results
Random Forest:
- Accuracy: 0.75
- F1 Score: 0.706

Gradient Boosting:
- Accuracy: 0.55
- F1 Score: 0.471

The Random Forest model was selected for deployment.

## Project Structure
chemical-hazard-prediction/
│
├── chemical_dataset_100.csv
├── cleaned_chemical_dataset100.csv
├── chemical_features_dataset.csv
├── chemical_hazard_model.pkl
├── app.py
├── requirements.txt


## How to Run

Install dependencies:

```bash
pip install pandas pubchempy rdkit tqdm scikit-learn seaborn matplotlib gradio joblib
```

Run the application:

```bash
python app.py
```

Open the generated local URL in your browser to use the prediction interface.

## Example Inputs
- benzene
- glucose
- CCO
- C1=CC=CC=C1
