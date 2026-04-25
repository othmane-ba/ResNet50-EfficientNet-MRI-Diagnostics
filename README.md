# ResNet50 vs EfficientNet-B0: A Comparative Analysis for Tumor Recognition
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.19749011.svg)](https://doi.org/10.5281/zenodo.19749011)
## Overview
This repository contains a direct, side-by-side comparative study between **ResNet50** and **EfficientNet-B0** for tumor recognition. The study focuses on evaluating the performance, accuracy, convergence speed, and loss of these two popular convolutional neural network architectures.

## Dataset
This project uses the **Masoud Nickparvar Brain Tumor dataset** for training and evaluation. The dataset provides a comprehensive set of MRI images for tumor classification.

## Methodology
- **Unified Training Pipeline:** A robust training function evaluates both models under identical conditions, integrating early checkpointing, L2 regularization, and Dropout to prevent overfitting.
- **Architectures Evaluated:** 
  - **ResNet50:** A standard 50-layer deep residual network.
  - **EfficientNet-B0:** A highly efficient CNN architecture that scales network width, depth, and resolution.
- **Advanced Evaluation & Explainability:** Beyond standard accuracy and loss tracking, the notebook includes:
  - Classification Reports for Precision, Recall, and F1-scores.
  - Confusion Matrices and ROC / AUC curves for deep multi-class evaluation.
  - Grad-CAM heatmap visualizations to interpret model focus areas on MRI scans.

## Repository Structure
- `ResNet50_vs_EfficientNet.ipynb`: The main notebook containing data handling, model training routines, and advanced evaluation metrics.
- `requirements.txt`: Required Python dependencies.
- `.gitignore`: Standard Git ignore file for datasets and virtual environments.

## Getting Started

### Prerequisites
- Python 3.8+
- Linux environment or Windows with WSL recommended (for stable PyTorch multiprocessing).
- NVIDIA GPU (optional, but highly recommended for fast training).

### Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone <your-github-repo-url>
   cd <your-repo-name>
   ```

2. **Create and activate a virtual environment:**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch the Notebook:**
   The dataset is downloaded automatically inside the notebook using `kagglehub`. Simply start Jupyter:
   ```bash
   jupyter notebook ResNet50_vs_EfficientNet.ipynb
   ```

## Results
At the end of the notebook, you will find side-by-side performance visualizations including training curves, multi-class confusion matrices, ROC curves, and Grad-CAM attention maps saved as high-resolution standard figures.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
