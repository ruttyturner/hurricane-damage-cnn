# Hurricane Damage Classification with CNN + LIME

A deep learning project that classifies hurricane damage severity from aerial imagery, with model interpretability analysis using LIME to understand what the model actually learned.

---

## Overview

After a hurricane, rapid damage assessment is critical for directing emergency response resources. This project explores whether a convolutional neural network can automatically classify damage severity from aerial images — and more importantly, whether its decisions are grounded in meaningful visual features rather than noise.

---

## Objectives

- Train a CNN to classify aerial images by hurricane damage severity
- Use LIME (Local Interpretable Model-Agnostic Explanations) to visualize which regions of each image influenced the model's predictions
- Validate that the model learned structurally meaningful damage features

---

## Methods

### Model
- Convolutional Neural Network (CNN) built with TensorFlow/Keras
- Architecture includes convolutional + pooling layers for spatial feature extraction, followed by dense classification layers
- Trained on labeled aerial imagery with damage severity categories

### Interpretability
- Applied **LIME** to generate local explanations for individual predictions
- LIME perturbs input images and fits a locally faithful linear model to identify which superpixels most influenced each classification
- Confirmed that highlighted regions corresponded to visible structural damage (e.g. destroyed rooftops, debris fields) rather than background features like vegetation or roads

---

## Key Results

- Model successfully distinguished between damage severity classes across held-out test images
- LIME visualizations revealed the model focused on structurally relevant regions, providing confidence that predictions are interpretable and not driven by spurious correlations

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| TensorFlow / Keras | CNN model building and training |
| scikit-learn | Evaluation metrics |
| LIME | Model interpretability |
| NumPy / Pandas | Data processing |
| Matplotlib | Visualization |

---

## Project Structure

```
hurricane-damage-cnn/
├── data/               # Image data (not included — course-provided)
├── notebooks/          # Jupyter notebooks for training and analysis
├── lime_outputs/       # LIME explanation visualizations
└── README.md
```

---

## Sample LIME Output

ADD

---

## What I Learned

This project reinforced that model accuracy alone is an incomplete measure of quality. Using LIME to audit the CNN's decision-making process revealed whether the model generalized meaningfully — a critical consideration in high-stakes applications like disaster response.
