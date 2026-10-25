# Causal Fairness Project Reproduction

This repository contains Jupyter notebooks focused on reproducing causal fairness experiments from key research papers.

## Project Overview

1. **Counterfactual Fairness**
   * **Paper:** *Counterfactual Fairness* (arXiv:1703.06856)
   * **Dataset:** Law School Admissions Bar Passage dataset
   * **Description:** Implements models ranging from a naive baseline to causal solutions to predict first-year academic performance (FYA) while maintaining counterfactual fairness regarding race and sex. It utilizes Pyro (built on PyTorch) for probabilistic programming and inference of latent variables.

2. **Fair Inference on Outcomes**
   * **Paper:** *Fair Inference on Outcomes* (Nabi & Shpitser, AAAI 2018 arXiv:1705.10378)
   * **Dataset:** Adult Dataset
   * **Description:** A Python translation and study of the paper's experiment predicting high income based on gender. It formulates discrimination as a path-specific effect (PSE) and employs constrained Maximum Likelihood Estimation via the COBYLA method to learn a fair distribution.

3. **Path-Specific Counterfactual Fairness**
   * **Paper:** *Path-Specific Counterfactual Fairness* — Silvia Chiappa & Thomas P.S. Gillam (DeepMind, 2018) (arXiv: 1802.08139)
   * **Dataset:** Berkeley Admission Dataset, UCI Adult Dataset, and UCI German Credit Dataset
   * **Description:** Implements the PSCF-VAE algorithm from scratch using PyTorch to run three experiments. The method corrects observations that are "tainted" by the sensitive attribute's unfair influence while preserving all fair information, which differs from prior work that imposed linear constraints on model parameters or averaged out entire mediator variables.

## Prerequisites

You need to have [Conda](https://docs.conda.io/en/latest/miniconda.html) or Miniconda installed on your system to manage the dependencies.

## Setup Instructions

**Step 1: Create the Conda Environment**
Navigate to the root directory containing the `environment.yaml` file and run:
```bash
conda env create -f environment.yaml
``` 

## Environment Setup & Running in VS Code

### Step 2: Activate the Environment

Once the installation is complete, activate your Conda environment:

```bash
conda activate fairness_env
```
### Step 3: Set Up and Run in VS Code

To run notebooks inside Visual Studio Code, follow these steps:

Open **Visual Studio Code**
Navigate to your project folder
Ensure you have these extensions installed:
1. Python
2. Jupyter

Select the Kernel
1. Open a notebook (e.g., counterfactual_fairness_final.ipynb)

2. Click “Select Kernel” (top-right)

3. Choose the interpreter corresponding to: fairness_env

### Run the Notebook

You’re now ready to go:

* Click Run All
* Or execute cells individually