# AIPI 590 - XAI | Assignment #04  
## Explainable Deep Learning — GradCAM and Its Variants  

**Author:** Jay Liu  
**Repository:** [jayliu1016/Xai_hw4](https://github.com/jayliu1016/Xai_hw4)  
**Google Colab Notebook:** [Open in Colab →](https://colab.research.google.com/github/jayliu1016/Xai_hw4/blob/main/notebook1.ipynb)

---
( The readme was paraphrased and structured by GPT5 at 10:50 p.m. on Oct 5th for better reading purpose.)

### 📘 Project Description  
This project explores **explainable deep learning** techniques in computer vision through the implementation of **GradCAM** and its two variants, **GradCAM++** and **EigenCAM**.  
The chosen domain is **Wildlife Detection in Conservation**, where the goal is to classify zebras versus other animals in natural images.  
Explainability is critical in this setting because conservation models must justify decisions that influence biodiversity monitoring and anti-poaching operations.

The notebook demonstrates how pretrained models like **ResNet-50** focus on visual regions that drive classification. It visualizes attention maps for multiple animal images and compares the interpretability performance across different GradCAM variants.

---

### 🧩 Techniques Implemented
- **GradCAM** — baseline method visualizing class-specific gradient activations.  
- **GradCAM++** — variant that refines localization using higher-order gradients.  
- **EigenCAM** — activation-based approach independent of gradients, providing smoother visual attributions.  

All three methods were applied to at least **five images**, sourced from **public GitHub research datasets** (e.g., YOLO, OpenVINO, and Darknet examples).

---

### 🖼️ Results Overview
- GradCAM and GradCAM++ focused primarily on the **body of the animal**, highlighting discriminative textures (e.g., zebra stripes).  
- EigenCAM provided smoother attention maps but occasionally emphasized broader, less specific regions.  
- Some misleading results occurred:
  - The **herd image** was misclassified as “ox,” despite correctly focusing on the group of striped animals.  
  - The **dog-and-bicycle** image showed attention leakage toward the bicycle, revealing contextual bias.  

These observations illustrate that correct spatial attention does not always imply correct conceptual understanding.

---

### 🧠 Reflection and Analysis
- **Model Focus:** GradCAM and its variants largely captured meaningful features like body texture and shape, which align with human intuition.  
- **Surprising Cases:** Misclassifications and context bias revealed weaknesses in the model’s internal representations.  
- **Explainability Significance:** In conservation, explainability ensures that automated detection tools can be trusted by domain experts and policymakers, promoting transparency and accountability in AI-driven biodiversity monitoring.

---

### 🧱 Project Structure
Xai_hw4/
├── notebookl.ipynb # Main Colab notebook
├── requirements.txt # Required dependencies
├── README.md # Project documentation
└── /images # (Optional) Local visualization outputs

---

### ⚙️ How to Run
1. Open the notebook directly in Colab:  
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jayliu1016/Xai_hw4/blob/main/model.ipynb)
2. Run all cells from top to bottom.  
3. The notebook will automatically:
   - Load pretrained ResNet-50  
   - Apply GradCAM, GradCAM++, and EigenCAM  
   - Display comparative attention visualizations  

---

### 📄 Academic Integrity Statement
All code was written manually without the use of AI assistance.  
Images used in this notebook were obtained from publicly available research examples on GitHub and open datasets for educational purposes only.

---

**Author:** Jay Liu  
📍 Duke University | MIDS 2026  
📧 [GitHub Profile](https://github.com/jayliu1016)

