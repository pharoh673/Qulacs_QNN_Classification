# Quantum Neural Networks for Binary Classification: Iris and Cancer Datasets with Qulacs

This repository implements a **Quantum Neural Network (QNN)** for **binary classification** on the **Iris** and **Cancer** datasets. Using **Qulacs**, a high-performance quantum simulator, we build and train quantum circuits for classification tasks, exploring both **Adam optimizer** and **Parameter-Shift gradient** methods for optimization.

## 🚀 **Project Overview**

This project demonstrates the application of **Quantum Machine Learning (QML)** for solving **binary classification** problems. The datasets used in this project are:
1. **Iris Dataset** (Setosa vs. Versicolor)
2. **Cancer Dataset** (Malignant vs. Benign)

We implement a **Variational Quantum Neural Network (QNN)** with:
- **Angle encoding** to map classical data to quantum states
- **Variational layers** composed of **RX**, **RY**, **RZ** rotations and **CNOT** gates for entanglement
- **Trainable quantum parameters** optimized using **Adam** or **Parameter-Shift SGD** optimizers

## 🛠️ **Technologies & Tools**

- **Qulacs**: High-performance quantum simulator for building and running quantum circuits.
- **Scikit-learn**: For data preprocessing, splitting, and evaluation.
- **NumPy**: For numerical operations.
- **Matplotlib**: For visualizations.

## 📊 **Project Components**

1. **Data Preprocessing**:
   - We load and preprocess the Iris and Cancer datasets.
   - The features are normalized to the range [0, π] to fit the quantum circuit encoding.

2. **Quantum Neural Network Design**:
   - **Qulacs** is used to create quantum circuits.
   - The variational circuit consists of **rotation gates** (RX, RY, RZ) and **CNOT gates** for entanglement.
   - The model output is measured using **Pauli-Z** operators.

3. **Gradient Optimization**:
   - **Parameter-Shift** and **Finite-Difference** gradient methods are implemented to update quantum parameters during training.
   - Two optimizers are used:
     - **Adam optimizer**: Faster convergence using numeric gradients.
     - **SGD optimizer with parameter-shift**: Exact gradients with a slower, more precise optimization process.

4. **Training & Evaluation**:
   - Models are trained using **Iris** and **Cancer** datasets.
   - **Accuracy** and **loss curves** are tracked over multiple epochs.
   - We compare the performance of the Adam and Parameter-Shift optimizers.

## ⚡ **Results**

- **Iris Dataset**: 
   - Achieved **100% accuracy** on training data.
   - **95% validation accuracy** using **4-qubit variational quantum circuit**.

- **Cancer Dataset**:
   - Achieved **98-100% accuracy** using **Parameter-Shift optimization** for exact quantum gradients.

## 📂 **Project Files**

- `iris_cancer_qnn.ipynb`: Jupyter notebook containing the quantum neural network model for the Iris and Cancer datasets.
- `data_preprocessing.py`: Script for loading and preprocessing the datasets.
- `qnn_model.py`: Contains the QNN circuit design and functions for training, prediction, and gradient computation.
- `optimizers.py`: Implementation of Adam and SGD optimizers with gradient functions.
- `utils.py`: Utility functions for accuracy evaluation and visualization.

## 📝 **How to Run**

To run the notebook and experiment with the model:

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/quantum-neural-network.git
   cd quantum-neural-network
