# Chasing the Trade-Off: A Pareto-based Multi-Objective Deep Reinforcement Learning Approach for Portfolio Management

This repository contains the official code, data (partial), and evaluation scripts for the AAAI submission:

**Chasing the Trade-Off: A Pareto-based Multi-Objective Deep Reinforcement Learning Approach for Portfolio Management**

---

## Overview

We propose a Pareto-based Multi-Objective Deep Reinforcement Learning (PMODRL) framework for portfolio Management, balancing return and risk. The method is validated on real-world financial datasets (S&P 500 and SSE 50), demonstrating strong performance against state-of-the-art baselines under multiple evaluation metrics.

---

## Repository Structure

```
.
├── code/                           # Main code directory
│ ├── train.py                      # Main training script
│ ├── evaluate_table_comparison.py  # Evaluation script (main results)
│ ├── evaluate_table_ablation.py    # Evaluation script (ablation study)
│ ├── model/                        # Saved models will be stored here
│ ├── evaluation/                   # Evaluation results will be saved here
│ └── data/                         # Processed data used by code
│   ├── data1_1925/                 # S&P500 data (2019–2025)
│   ├── data1_1824/                 # S&P500 data (2018–2024)
│   ├── data2_1925/                 # SSE50 data (2019–2025)
│   └── data2_1824/                 # SSE50 data (2018–2024)
├── data/                           # Raw input data folder
│ ├── SP500/                        # Raw/preprocessed data for S&P 500
│ └── SSE50/                        # Partial raw data for SSE50 (privacy restricted)
├── requirements.txt                # Python dependencies
```

---

## Environment Setup

- Python 3.8.20
- PyTorch 2.1.2
- CUDA 12.1

### Install dependencies:

```bash
pip install -r requirements.txt
```

---

## How to Run

### Step 1: Train and Test

```bash
python train.py
```

Results will be saved to the `model/` directory.

### Step 2: Evaluate the performance

```bash
python evaluate_table_comparison.py
python evaluate_table_ablation.py
```

Evaluation results will be saved in the `result_evaluation/` directory.

---

## Data

- **data1: S&P 500**: Full raw dataset is provided under data/SP500/. Processed versions used in training are in code/data/data1_1925/ (2019–2025) and code/data/data1_1824/ (2018–2024).
- **data2: SSE 50**: Partial raw data is provided under data/SSE50_partial/ due to confidentiality. Processed subsets are in code/data/data2_1925/ (2019–2025) and code/data/data2_1824/ (2018–2024).

All datasets have been preprocessed. No additional data processing is required before training.

---

## License

This code is made available for academic review and reproduction of the ICSA submission only. Redistribution of the code or data for commercial use is not permitted.





