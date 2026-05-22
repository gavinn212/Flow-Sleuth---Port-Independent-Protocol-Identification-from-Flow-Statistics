# Network Protocol Identification from Flow Statistics

A machine learning project for port-independent network protocol identification 
and intrusion detection using flow-level statistical features.

## Overview

Traditional network protocol identification relies on port numbers, which can 
be easily evaded by modern applications and attackers. This project classifies 
network traffic using only flow-level statistics (e.g., packet size, duration, 
inter-arrival time), making it robust against port-based obfuscation.

The model was first validated on synthetic data, then scaled to the real-world 
CICIDS2017 benchmark dataset containing over 2.3 million network flow samples.

## Results

| Dataset | Samples | Classes | Baseline | Final Accuracy |
|---------|---------|---------|----------|----------------|
| Synthetic | 100K | 5 protocols | 54.8% | 81.4% |
| CICIDS2017 | 2.3M | 15 attack types | 81.6% | 95–99% |

## Tech Stack

- **Language**: Python
- **ML**: scikit-learn (Random Forest)
- **Data Processing**: Pandas, NumPy
- **Environment**: Jupyter Notebook

## Dataset

- **Synthetic**: Generated 100K samples across 5 protocol classes for initial 
model development
- **CICIDS2017**: Real-world intrusion detection dataset containing 2.3M labeled 
network flows across 15 categories including DDoS, PortScan, Brute Force, and 
Botnet traffic

## Project Structure
├── Protocol_Identification_final.ipynb         # Synthetic data experiments
├── Protocol_Identification_new_data_set.ipynb  # CICIDS2017 real-world experiments
├── dataset.zip                                  # Dataset files
└── README.md

## How to Run

1. Clone the repository
```bash
   git clone https://github.com/newguy75/Flow-Sleuth---Port-Independent-Protocol-Identification-from-Flow-Statistics.git
```
2. Install dependencies
```bash
   pip install pandas numpy scikit-learn jupyter
```
3. Open and run either notebook in Jupyter

## Authors

- **Zeyu Peng (Ben)** — [@newguy75](https://github.com/newguy75)
- **Gavin** — [@gavinn212](https://github.com/gavinn212)
