# FlakyXbert: Flaky Test Detection and Classification Framework


## Overview

FlakyXbert is a machine learning framework designed to detect flaky tests in software projects and classify them into root causes of flakiness. Flaky tests exhibit non-deterministic behavior, leading to unreliable test results and increased maintenance costs. Our approach leverages the **FlakyXbert** model to analyze test data from multiple datasets, including FlakyCat and IDoFT, to enhance prediction accuracy and robustness.

## Datasets

### FlakyCat Dataset
The FlakyCat dataset contains information on flaky tests identified across various software projects. It includes baseline and updated test files used for training and evaluating the FlakyXbert model.

- **Location:** `dataset/FlakyCat_data/`
- **Key Files:**
  - `test_files_v0/`: Baseline test files.
  - `test_files_v12/`: Augmented test files.

### IDoFT Dataset
The IDoFT dataset focuses on flaky tests within the IDoFT framework, providing both binary classification tasks and project-specific analyses to improve model generalization.

- **Location:** `dataset/IDoFT_data/`
- **Key Files:**
  - `Flakify_IDoFT_dataset.csv`
  - `IDoFT_dataset.csv`

## Codebase

The codebase is organized into two main sections, each corresponding to a dataset:

### FlakyCat Dataset Code
Located in `src/FlakyCat_dataset_code/`, this section contains Jupyter notebooks that implement various experiments and models using the FlakyCat dataset.

### IDoFT Dataset Code
Located in `src/IDoFT_dataset_code/`, this section includes Jupyter notebooks tailored for the IDoFT dataset, featuring binary classification and project-wise models.

### Utility Notebooks
- `calculate.ipynb`: Scripts for calculating key metrics and performance indicators.
- `FlakyXbert_augExperiment1.ipynb` & `FlakyXbert_augExperiment2.ipynb`: Additional Experiments with data augmentation that are not included in the paper.

## Getting Started

### Prerequisites

Ensure you have the following installed:
- Python 3.8 or higher
- Jupyter Notebook
- Required Python libraries (listed in `requirements.txt`)

### Installation

1. **Download the Files**


2. **Create a Virtual Environment**

    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3. **Install Dependencies**

    ```bash
    pip install -r requirements.txt
    ```

4. **Download Datasets**

    Place the `FlakyCat_data` and `IDoFT_data` directories inside the `dataset/` folder. Ensure the CSV files `Flakify_IDoFT_dataset.csv` and `IDoFT_dataset.csv` are correctly placed.

### Running the Notebooks

Launch Jupyter Notebook and navigate to the desired notebook within the `src/` directory:

```bash
jupyter notebook

