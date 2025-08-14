---

# Exoplanet Detection Using Convolutional Neural Networks (CNNs)

## 📌 Project Overview

This project applies **deep learning** techniques—specifically **Convolutional Neural Networks (CNNs)**—to detect exoplanets from **flux time-series data** collected by the **NASA Kepler Space Telescope**.

Exoplanets are planets that orbit stars outside our solar system. The **transit method** is used here: when a planet passes in front of its star, it causes a slight dip in the star’s brightness. This periodic dimming can be detected and classified using machine learning.

---

## 🛰 Dataset

* **Source:** NASA Kepler mission
* **Observations:** Over 3,000 flux values per star
* **Label meanings:**

  * `1` → Star with at least one exoplanet
  * `0` → No exoplanet detected

---

## ⚙ Workflow

1. **Data Preprocessing**

   * Shuffle and split into training/testing sets (80/20)
   * Separate features (flux values) from target (label)
   * Reshape data for CNN input

2. **Visualization**

   * Flux graphs for stars with/without exoplanets
   * Pairplots & KDE plots for exploratory data analysis
   * Confusion matrix for model performance

3. **Model Architecture**

   * Multiple **Conv1D** layers with Batch Normalization
   * **MaxPooling1D** for feature reduction
   * **Global Average Pooling** for generalization
   * Dense layers with Dropout for classification
   * **Sigmoid activation** for binary classification

4. **Training**

   * Optimizer: Adam (`learning_rate=0.0005`)
   * Loss: Binary Crossentropy
   * Metrics: Accuracy
   * Validation split: 20% of training data

5. **Evaluation**

   * Thresholded predictions at 0.5
   * Confusion matrix visualization
   * Accuracy, precision, recall metrics

---

## 📊 Model Summary

* **Input:** Flux time-series data
* **Output:** Binary classification (Exoplanet / No Exoplanet)
* **Performance:** High accuracy on test data
* **Future Improvements:**

  * Explore attention-based architectures
  * Integrate multi-spectral data
  * Tune hyperparameters for optimal performance

---

## 🚀 Getting Started

### Prerequisites

Install Python dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow
```

### Run the Notebook

1. Clone this repository:

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME
```

2. Launch Jupyter Notebook:

```bash
jupyter notebook
```

3. Open the notebook and run all cells sequentially.

---

## 📌 Example Visualizations

### Flux Graph — Star with Exoplanet

![Flux Graph With Exoplanet](images/flux_with_exoplanet.png)

### Flux Graph — Star without Exoplanet

![Flux Graph Without Exoplanet](images/flux_without_exoplanet.png)

### Pairplot of Features

![Pairplot](images/pairplot.png)

### KDE Plot of Flux.1

![KDE Plot](images/kde_flux1.png)

### Confusion Matrix

![Confusion Matrix](images/confusion_matrix.png)

---

## 📚 References

* [NASA Kepler Mission Data](https://www.nasa.gov/mission_pages/kepler/main/index.html)
* [TensorFlow Documentation](https://www.tensorflow.org/api_docs)

---

## 🏆 Acknowledgments

This project draws inspiration from research in **AI for astronomy** and competitions like the **Kepler exoplanet detection challenge**.

---
