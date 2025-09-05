
# Project Title

A brief description of what this project does and who it's for

# 📂 Data Guide

This project uses **Human Connectome Project (HCP 2020)** data.  
Because of licensing restrictions, the raw HCP fMRI data is **not included** in this repository.  

---

## 📌 Dataset Information

- **Source:** [Human Connectome Project (HCP)](https://www.humanconnectome.org/study/hcp-young-adult)  
- **Subjects:** 339 unrelated healthy adults  
- **Modalities used:**  
  - Resting-state fMRI (60 minutes per subject)  
  - Working Memory (WM) task fMRI (2-back / 0-back blocks)  

---

## 🛠️ How We Accessed It

During the **Neuromatch Academy 2025 (Computational Neuroscience track)**, we were provided with a **starter notebook** that:  
- Loaded preprocessed HCP data (via Neuromatch data servers)  
- Included cortical parcellation (360 regions, Glasser atlas)  
- Offered initial exploratory plots and matrix structures  

The notebook is included in [`load_hcp`](https://github.com/NeuromatchAcademy/course-content/blob/main/projects/fMRI/load_hcp.ipynb) for reproducibility.

---

## 📥 How To Access HCP Data Yourself

1. Register and apply for access to the HCP dataset:  
   👉 [HCP Database Access Instructions](https://db.humanconnectome.org)  

2. Download:  
   - Resting-state fMRI  
   - Working memory task fMRI  

3. Preprocess with the **HCP minimal preprocessing pipeline**, or reuse the preprocessed versions provided by HCP.

---

## 📂 Data Structure (in analyses)

After loading and preprocessing, our data is structured as:

- **Cortical area × time matrices** (360 regions × T timepoints)  
- Time series segmented into:  
  - **Resting runs**  
  - **Working Memory task blocks**  
  - **Inter-task intervals**  

These matrices were the input for PCA, k-means, HMM, and t-SNE analyses.

---

