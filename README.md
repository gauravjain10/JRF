# Jointly Robust Fairness (JRF)

Official implementation of the paper **"Jointly Robust Fairness: Overcoming Simultaneous Label and Attribute Noise"** (NeurIPS 2026).

---

## 📌 Overview
This repository provides the complete implementation of the **Jointly Robust Fairness (JRF)** framework, which guarantees algorithmic fairness in the presence of simultaneous label and sensitive attribute noise.

### Highlights:
- **True Joint Robustness:** Combines Forward Loss correction for corrupted target labels with Matrix-Inverse Robust Loss (MIRL) for corrupted sensitive attributes.
- **Asymmetric Noise Generalization:** Extends closed-form matrix inversion to group-skewed noise distributions ($\rho_{01} \neq \rho_{10}$).
- **Benchmark Coverage:** Full reproducible pipelines on the **Adult**, **Bank Marketing**, and **COMPAS** datasets.
- **Minimal Overhead:** Single-pass closed-form training with zero requirement for clean validation data.

---

## 🛠️ Repository Contents
- `JRF.ipynb`: Self-contained Jupyter Notebook reproducing all benchmark sweeps, ablation studies, and figure generations.
- `requirements.txt`: Python package dependencies.
- `README.md`: Instructions and overview.

---

## 🚀 Getting Started

### Option 1: Run in Google Colab (Recommended)
1. Open [Google Colab](https://colab.research.google.com/).
2. Upload `JRF.ipynb`.
3. Select **Runtime > Run all**. The notebook automatically downloads the OpenML datasets, trains the models across 5 seeds, and saves all 7 PDF figures.

### Option 2: Run Locally
Clone the repository and install the dependencies:
```bash
git clone https://github.com/<your-username>/JRF.git
cd JRF
pip install -r requirements.txt
jupyter notebook JRF.ipynb


📄 Citation
If you find this work or code useful, please cite our paper:

Bibtex
@inproceedings{jain2026jointly,
  title={Jointly Robust Fairness: Overcoming Simultaneous Label and Attribute Noise},
  author={Jain, Gaurav},
  booktitle={Advances in Neural Information Processing Systems (NeurIPS)},
  year={2026}
}
