# Network Intrusion Detection with Two-Phased Hybrid Ensemble Learning and Automatic Feature Selection (THE-AFS)

A machine learning-based Network Intrusion Detection System (NIDS) that combines automatic feature selection with a two-phased hybrid ensemble learning framework to detect known and unknown network attacks with high accuracy and low false alarm rates.

## Problem Statement
Modern network devices generate massive volumes of high-dimensional traffic data, making it difficult for traditional NIDS to accurately detect both known and unknown attacks. Manual feature selection is error-prone and inefficient at scale.

## Proposed Solution (THE-AFS)
This project introduces a Two-Phased Hybrid Ensemble with Automatic Feature Selection (THE-AFS):

### Core Innovation 1 — Automatic Feature Selection
Four ML classifiers (Decision Tree, Random Forest, ANN, SVM) independently rank features by importance, automating what is typically a manual and error-prone process. The most significant features are selected based on combined classifier rankings.

### Core Innovation 2 — Two-Phased Hybrid Ensemble Learning
- **Phase 1:** One-vs-One classification framework flags potential attack candidates from normal traffic
- **Phase 2:** Multiclass classifiers narrow flagged candidates down to a specific attack class

## Datasets
| Dataset | Type | Description |
|---------|------|-------------|
| NSL-KDD | Wired | Benchmark dataset for wired network intrusion detection |
| AWID | Wireless | Benchmark dataset for wireless network intrusion detection |

## Results
- **THE-AFS-DT** achieved best performance on the NSL-KDD (wired) dataset
- **THE-AFS-RF** achieved best performance on the AWID (wireless) dataset
- Both variants outperformed comparable studies in detection rate and false alarm rate

## Repository Structure
network-intrusion-detection-hybrid-ensemble-afs/
│
├── data/nsl-kdd/               # NSL-KDD dataset files
├── static/                     # Static assets for web app
├── templates/                  # HTML templates for web app
├── AWIDS.ipynb                 # Notebook for AWID wireless dataset
├── NSL-KDD.ipynb               # Notebook for NSL-KDD wired dataset
├── app.py                      # Flask web application
├── model_nsl.sav               # Saved trained model (NSL-KDD)
├── nslkdd_processed.csv        # Preprocessed NSL-KDD data
├── processed.csv               # Processed dataset
├── sample_full.csv             # Full sample data
├── y_train.csv                 # Training labels
├── signup.db                   # User database for web app
├── README.md
## Tech Stack
- Python
- Scikit-learn
- Pandas
- NumPy
- Flask (web application)
- Jupyter Notebook
- Anaconda

## How to Run

### Run the Notebooks
1. Clone the repository
```bash
git clone https://github.com/Komatireddy20/network-intrusion-detection-hybrid-ensemble-afs
cd network-intrusion-detection-hybrid-ensemble-afs
```
2. Install dependencies
```bash
pip install scikit-learn pandas numpy flask jupyter
```
3. Open the notebooks
```bash
jupyter notebook NSL-KDD.ipynb
jupyter notebook AWIDS.ipynb
```

### Run the Web Application
```bash
python app.py
```

## Team
Developed as part of B.Tech final year project at Vignana Bharathi Institute of Technology (2023-24).
Project Lead: Sravya Komati Reddy
