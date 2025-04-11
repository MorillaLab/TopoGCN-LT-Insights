# TopoGCN-LT-Insights
[![License](https://img.shields.io/badge/License-MIT-green)](https://opensource.org/license/mit/)
[![Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://github.com/MorillaLab/TopoGCN-LT-Insights/tree/main/Graphical_learning/)


# TDA-aided Graph Convolutional Networks for improved lung transplantation insights.
The Lung Transplant Prediction Dataset is a comprehensive collection of medical and demographic records from patients, including their lung transplant outcomes (positive or negative). The dataset encompasses key features such as age, gender, body mass index (BMI), mean pulmonary artery pressure (MPAP), presence of heart and bronchial diseases, preoperative diabetes, acute renal failure, pneumonia, among others.

This dataset serves as a valuable resource for constructing machine learning models aimed at predicting the one-year mortality risk following a lung transplant. Leveraging patients' medical histories and demographic details, these models empower healthcare professionals to identify individuals with an elevated risk of requiring a lung transplant, facilitating the development of tailored treatment plans.

Beyond clinical applications, researchers can utilize this dataset to investigate intricate relationships between diverse medical and demographic factors and the probability of undergoing a lung transplant. The insights gleaned from such analyses can contribute to a deeper understanding of the complex interplay between health indicators and the likelihood of lung transplantation.


    %% Fig1a - Encoding
    A[FASTA Input] --> B[DNA-BERT]
    B --> C[Per-AA Embeddings\n768D, LayerNorm]
    C --> D[RL Agent]
    D --> E[Optimal 768D Rep]
    
    %% Fig1b - Topology
    E --> F[Persistent Homology\nH₀,H₁,H₂]
    F --> G[Wasserstein Metric\np=2]
    
    %% Fig1c - CNN
    E --> H[Image Reshape]
    H --> I[LeNet-5]
    I --> J[Cross-Entropy Loss]
    
    %% Backprop
    J -->|∂ℒ/∂W| I
    J -->|Approx. ∂ℒ/∂H₁| F
    J -->|REINFORCE| D
