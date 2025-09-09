# Comparative Analysis of Dimensionality Reduction Methods on Single-Cell RNA-seq Data

This repository contains the implementation and evaluation of four popular dimensionality reduction methods applied to single-cell RNA sequencing (scRNA-seq) datasets.  
The work is based on the article *[A Comparison for Dimensionality Reduction Methods of Single-Cell RNA-seq Data](https://doi.org/10.3389/fgene.2021.646936)*.

---

## 📌 Overview
Single-cell RNA-seq data are inherently high-dimensional, sparse, and noisy. 

In this project, I implemented and compared the following four methods:
- **PCA (Principal Component Analysis)** – Linear method, baseline for dimensionality reduction  
- **t-SNE (t-distributed Stochastic Neighbor Embedding)** – Nonlinear, excels at local structure preservation  
- **UMAP (Uniform Manifold Approximation and Projection)** – Nonlinear, balances local and global structures with high stability  
- **VAE (Variational Autoencoder)** – Neural network–based, captures nonlinear latent features  

---

## 📂 Datasets
We evaluate the methods on three benchmark scRNA-seq datasets:

- **Deng**: Mouse early embryonic development (zygote to blastocyst) – [GSE45719]  
- **Chu**: Human embryonic stem cell differentiation to progenitor cells – [GSE75748]  
- **PBMC68k**: Large-scale dataset of 68,000 human peripheral blood mononuclear cells – [10x Genomics]  

---

## ⚙️ Methods & Evaluation
Each dimensionality reduction method was applied to the normalized gene expression matrices of the above datasets.  

We assessed performance using clustering and embedding quality metrics:
- **Adjusted Rand Index (ARI)**  
- **Normalized Mutual Information (NMI)**  
- **Silhouette Score**  

We also evaluated **computational cost** (runtime, memory usage) on the datasets.

---

## 📊 Results (Summary)
- **t-SNE**: Highest accuracy but higher computational cost  
- **UMAP**: Most stable, good balance between accuracy and scalability  
- **PCA**: Fast and efficient, but less effective on heterogeneous datasets  
- **VAE**: Competitive accuracy, flexible for capturing nonlinear structures  

*(See notebook for detailed plots and comparisons.)*

