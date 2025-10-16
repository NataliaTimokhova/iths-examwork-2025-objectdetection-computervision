<h1 align="center">🎓 IT-Högskola (ITHS)</h1>
<h2 align="center">Exam Work (Examensarbete) – AI 2025</h2>
<h2 align="center">Object Detection & Computer Vision</h2>
<h3 align="center">Stockholm, Sweden – June 2025</h3>

<br>

<p align="center">
  <strong>Final Exam Work (Examensarbete)</strong> conducted at <strong>IT-Högskola (ITHS)</strong> as part of the <strong>AI 2025</strong> program.<br>
  Developed during the <strong>LIA2 internship</strong> at <strong>TrAI AB</strong>, Enköping, Sweden.
</p>

<br>

<p align="center">
  <em>Comparison of deep learning architectures (<strong>ResNet18</strong> vs <strong>ResNet50</strong>) for black-and-white symbol recognition using local GPUs.</em><br>
  Focused on <strong>object detection</strong> and <strong>computer vision</strong> with <em>PyTorch</em>.
</p>

<br>

---

## About

This repository documents my **final exam work (Examensarbete)** completed during the **LIA2** internship at the AI startup **TrAI AB** (Enköping, Sweden).  
The project explores **computer vision** methods for recognizing **black-and-white electrical symbols** on a fully **local training pipeline** (no cloud dependency).

The study compares **ResNet18** and **ResNet50** in terms of accuracy, convergence, and resource usage when trained and evaluated on **in-house GPUs**.


---

## Project Details

- **School / Program:** ITHS — AI 2025  
- **Internship:** LIA 2 (Work-Based Learning) at TrAI AB  
- **Location:** Enköping, Sweden
- **Language:** Swedish
- **Date:** **June 2025**  
- **Author:** Natalia Timokhova

---

## Aim

Build a **fully local, automated image classification pipeline** that:

- removes dependency on cloud platforms (e.g., using Roboflow only for manual labeling if needed),  
- ensures **full control** over training and inference,  
- preserves **data integrity** by keeping sensitive data on-prem,  
- enables **cost-efficient** experimentation on company hardware.

---

## Research Questions (Theses)

1. Can locally trained models with open tools (PyTorch) reach high accuracy **without** cloud services?  
2. How do **ResNet18** and **ResNet50** compare in **accuracy**, **convergence**, and **GPU/memory** usage?  
3. Are **simpler architectures** sufficient (or even preferable) for practical symbol recognition in production?

---

## Method Summary

- **Task:** Multiclass classification of black-and-white electrical symbols (5 classes: *1-polig*, *dimmer*, *dubbeltrapp*, *kron*, *trapp*).  
- **Dataset:** 9,255 images (≈ **98% synthetic**, ≈ **2% real**).  
- **Preprocessing:** 224×224 resize, ImageNet normalization; horizontal flip augmentation.  
- **Models:** **ResNet18** and **ResNet50** (ImageNet pre-trained; full fine-tuning).  
- **Training:** Adam (lr=1e-3), batch size 50, up to 40 epochs, checkpoints on best validation accuracy, trained on **local GPUs**.  
- **Evaluation:** Overall & per-class accuracy, convergence behavior, and resource efficiency; special focus on **generalization to real images**.

---

## Results & Conclusions (Short)

- On **real images**, **ResNet18** reached **87.5%** accuracy vs **68.75%** for **ResNet50**.  
- **ResNet18** trained faster (~**23 min** vs **25 min**) and used **less GPU memory**.  
- **ResNet50** showed signs of **overfitting to synthetic data**, with weaker real-world generalization.  

**Conclusion:**  
A **simpler architecture (ResNet18)** can outperform deeper networks in real-world settings when data is limited or dominated by synthetic samples. A **local GPU pipeline** provides better control, lower cost, and independence from commercial clouds - well suited for small AI companies.

---

## Confidentiality

> The **source code is not included** due to **company confidentiality** at TrAI AB.  
> This repository provides documentation and a summarized report of the work and findings.

---

## Reference

**Thesis:** *Object Detection and Computer Vision – Comparative Study of Deep Learning Architectures for Symbol Recognition*  
by **Natalia Timokhova**, ITHS AI 2025, conducted during **LIA2** at **TrAI AB**, Enköping, Sweden, **June 2025**.

---

## Acknowledgements

Thanks to **TrAI AB** for supervision and access to hardware, and to **ITHS** for academic guidance during LIA2.

