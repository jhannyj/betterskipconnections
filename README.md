# SkipTrace: Geometric Inference of Latent Architectural Shortcuts

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jhannyj/SkipTrace/blob/main/residual_geometry_inference.ipynb)

SkipTrace is a research project investigating whether skip connections leave a permanent geometric "fingerprint" on a neural network's internal representations
even when the physical shortcut is removed.

---

## Project Documentation & Analysis

The full research thesis, methodology, and experimental results (including the current **0.74 ROC AUC** findings) are documented inside the main analysis notebook.

**[Click here to view the Analysis Notebook](./notebooks/residual_geometry_inference.ipynb)**

*This notebook contains:*
* The Teacher-Student (SkipMLP vs. CopyMLP) distillation framework.
* Probing techniques including Kernel CKA and Causal Perturbation.
* Detailed analysis of gradient manifolds as architectural detectors.

---

## TODOS
- [ ] Refactor core logic from notebook into modular `.py` scripts (`models.py`, `metrics.py`).
- [ ] Refactor core logic to support local directory or Google Drive mount.
- [ ] Test the detector on standard architectures (e.g., deep VGG-style MLPs) not trained via distillation.
- [ ] Test real-time skip-connection insertion during the training phase.

---

## Getting Started

You can explore this research either locally or directly in your browser via Google Colab.

### **Option 1: Google Colab (Recommended)**
The fastest way to run the analysis is through Google Colab. Since the project uses modular `.py` scripts, the notebook includes a setup cell to clone the environment automatically.

1. Open the main notebook: **[Launch residual_geometry_inference.ipynb on Colab](https://colab.research.google.com/github/jhannyj/SkipTrace/blob/main/residual_geometry_inference.ipynb)**
2. Run the **"Environment Setup"** cell at the top to clone the repository and initialize the Python path.

---

### **Option 2: Local Installation**
If you prefer to run the experiments locally, ensure you have Python 3.8+ installed.

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/jhannyj/SkipTrace.git](https://github.com/jhannyj/SkipTrace.git)
   cd SkipTrace