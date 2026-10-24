# UMAP-MNIST-Reproduction

## Overview
This repository contains a Python implementation reproducing the primary MNIST dimensionality reduction experiment from the research paper *UMAP: Uniform Manifold Approximation and Projection for Dimension Reduction* (McInnes, Healy, & Melville, 2018). 

This project demonstrates the extraction of topological manifolds from high-dimensional image data (784 dimensions) and projects them into a 2D spatial embedding using the UMAP algorithm.

## Dataset
The data used in this reproduction is the **MNIST Database of Handwritten Digits**.
* **Source:** The dataset is fetched dynamically via the `scikit-learn` API using `fetch_openml('mnist_784', version=1)`.
* **Details:** It consists of 70,000 grayscale images of handwritten digits (0-9), where each image is 28x28 pixels.

## Original References
This reproduction is based entirely on the mathematical framework and baseline parameters established by the original authors.
* **Original Paper:** [arXiv:1802.03426](https://arxiv.org/abs/1802.03426)
* **Original Python Implementation:** [lmcinnes/umap](https://github.com/lmcinnes/umap)
* **Authors:** Leland McInnes, John Healy, and James Melville. 

## Environment & Dependencies
The code is written in Python and compiled within a Quarto (`.qmd`) environment. To execute the code, the following packages are required:
* `pandas`
* `numpy`
* `matplotlib`
* `umap-learn`
* `scikit-learn`

## Execution
The code is structured into three primary phases:
1. **Data Setup:** Fetches the 70,000 MNIST images via OpenML.
2. **Algorithm Execution:** Fits the UMAP reducer using hyperparameter baselines `n_neighbors=15`, `min_dist=0.1`, and `metric='euclidean'`.
3. **Visualization:** Plots the resulting 2D topological clusters using `matplotlib`.
