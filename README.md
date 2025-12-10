# How Depth and Width Affect the Representational Power of Multilayer Perceptrons

## Overview
This repository contains the code, figures, and supporting materials for the tutorial titled "How Depth and Width Affect the Representational Power of Multilayer Perceptrons." The tutorial examines how architectural choices in multilayer perceptrons, specifically depth (number of layers) and width (number of neurons per layer), influence representational capacity, gradient behaviour, and overall classification performance. Using a two-class nonlinear synthetic dataset, multiple MLP architectures were trained to compare the effects of increasing depth and width under controlled experimental conditions. Decision boundary plots, accuracy results, and confusion matrices are used to interpret how these architectural modifications affect model behaviour.

## Repository Structure
The repository is organised as follows:

├── notebook/  
│   └── mani_code_ml.ipynb                # Full experimental code  
├── figures/  
│   ├── depth_decision_boundaries.png  
│   ├── width_decision_boundaries.png  
│   ├── confusion_depth.png  
│   ├── confusion_width.png  
│   └── accuracy_tables.png                          # Optional exported tables  
├── README.md                                         # This documentation file  
└── LICENSE                                           # MIT license  

## Experiment Description

### 1. Goal
The aim of this project is to analyse how depth and width individually affect the expressive capacity and generalisation performance of multilayer perceptrons. Models were trained with varying numbers of layers and neurons to observe changes in decision boundaries, classification accuracy, and misclassification patterns.

### 2. Architectural Variations
Two sets of architectures were evaluated.

Depth variants:
(20), (20, 20), (20, 20, 20), (20, 20, 20, 20)

Width variants:
(5, 5), (20, 20), (50, 50), (100, 100)

All other hyperparameters remained constant across experiments.

### 3. Dataset
The experiments use the two-class "moons" dataset, which forms two interlocking semicircular shapes. It is well suited for assessing nonlinear representational capacity and allows clear visual comparison of decision boundaries. The data were standardised and split into training and test sets.

## How to Run the Notebook

1. Clone this repository:
git clone https://github.com/manikanta444-tech/machinelearning.git  
cd mlp-depth-width-analysis

2. Install dependencies:
pip install -r requirements.txt

3. Open the notebook:
jupyter notebook notebook/depth_width_experiments.ipynb

4. Run all cells to reproduce:
- Decision boundary figures  
- Confusion matrices  
- Accuracy tables  
- All comparative results  

## Key Findings
The experiments show that depth and width influence representational behaviour in distinct ways. Increasing depth can refine hierarchical modelling but produces diminishing returns beyond a small number of layers for moderately complex datasets. Increasing width primarily improves the model’s ability to form smooth nonlinear boundaries, with significant gains from narrow to moderate widths. Extremely wide architectures exhibit early signs of overfitting, as indicated by rising training accuracy without corresponding improvement in test accuracy. Confusion matrices confirm that narrow networks underfit, whereas moderately wide networks reduce misclassification across both classes.

## Citation
[Gubbala Leela Manikanta] (2025). "How Depth and Width Affect the Representational Power of Multilayer Perceptrons." GitHub Repository: https://github.com/yourusername/mlp-depth-width-analysis

## License
This project is released under the MIT License, allowing reuse for educational and research purposes.
