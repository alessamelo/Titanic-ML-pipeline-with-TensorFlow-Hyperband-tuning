#  Titanic Survival Prediction (Deep Learning + Hyperband)

This project implements an end-to-end machine learning pipeline to predict passenger survival on the Titanic dataset using a neural network optimized with **Hyperband (Keras Tuner)**. It includes automated preprocessing, hyperparameter tuning, threshold optimization, and comprehensive model evaluation.


##  Preprocessing Pipeline

A custom `DataFramePreparer` class is used to:

- Automatically detect feature types
- Handle missing values:
  - Median (numerical)
  - Most frequent (categorical)
- Apply:
  - Standard scaling (numerical)
  - One-hot encoding (categorical)
- Return a clean, model-ready dataset


##  Model

A fully connected neural network is used:

- Input layer based on number of features
- Tunable:
  - Number of layers
  - Number of neurons per layer
  - Activation function (`relu`, `tanh`)
  - Learning rate
- Output layer:
  - Sigmoid activation (binary classification)


##  Hyperparameter Optimization

Hyperparameters are optimized using **Keras Tuner - Hyperband**:


##  Early Stopping

To avoid overfitting:
* Monitors validation loss
* Stops training when performance plateaus
* Restores best model weights

##  Evaluation Metrics

The model is evaluated using:

* **Accuracy**
* **AUC (ROC)**
* **Precision**
* **Recall**
* **F1-score**
* **Confusion Matrix**


##  Technologies Used

* Python
* TensorFlow / Keras
* Keras Tuner
* Scikit-learn
* Pandas / NumPy
* Matplotlib / Seaborn
