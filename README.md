# MLP-Underfit-Overfit

Deep Learning Project: Shuttle Data Classification

This repository contains a project that implements and trains a deep learning model for a classification task on the Shuttle dataset. This class project focuses on the end-to-end process of building a robust model, including data handling, model training with hyperparameter tuning, and final evaluation.

**Project Objectives**

The main goals of this project were to:

**Data Preparation:** 📊 To handle a non-standard dataset format and prepare it for a deep learning model.

**Hyperparameter Optimization:** ⚙️ To systematically find the optimal learning rate and weight decay for the model.

**Model Training and Evaluation:** 🏋️ To train a model and analyze its performance, including identifying and mitigating overfitting.

**Key Project Steps**

The project was completed in the following stages:

**1. Dataset Preparation**
  📚 The dataset was loaded from the data folder.
  
  📦 The compressed training dataset was uncompressed and converted to a CSV format for processing. The read_file function was used for this purpose.
  
  🔪 The train dataset was split into training and validation sets with a test size of 0.3.
  
  🏷️ The **last column** was used as the **label**, with the remaining columns serving as input features.
  
  ✅ The data was batched using a DataLoader.
  
**2. Neural Network Model Definition**

  🧠 A suitable Multilayer Perceptron (MLP) model was defined, taking into account the number of classes in the dataset. An appropriate activation function was used.
  
**3. Device Selection**

  🚀 The model was moved to a GPU for faster training.

**4. Loss Function and Optimizer Definition**

  📉 The Cross-Entropy loss function and the SGD optimizer were defined.
  
**5. Model Training and Hyperparameter Tuning**

  A custom training and testing function was defined.
  
  
  **Forward and Backward Pass Check:** A small batch of data was used to check the forward pass, and a small subset of the training data was used to check the backward pass over 10 epochs.

  **Optimal Learning Rate Selection:** 🔍 The model was trained for one epoch with different learning rates (0.1, 0.01, 0.001, 0.0001) to find the most suitable starting value.

  **Small Grid Search:** A more precise learning rate and weight decay value were determined by training the network for 5 epochs and performing a grid search around the initial learning rate.
  
  **Final Training:** 📈 The model was then trained for a larger number of epochs using the optimal hyperparameters found in the previous steps.

**6. Results**

  📊 The learning curve (loss and accuracy over epochs) for the fully trained model was plotted.
  
  📉 The model was analyzed to determine if it was underfitting, overfitting, or a good fit.
  
**7. Model Saving and Evaluation**

  💾 The trained model was saved to a file.
  
  ⚙️ The saved model was used to predict on the separate test dataset.
  
  📤 The final predictions were saved to a predictions.csv file with a single pred column.
  
**8. Optional Overfitting & Dropout Analysis**

  🧠 The network was deliberately made to overfit by adding more layers and/or neurons. The learning curve was plotted to show the overfitting.
  
  ✨ Dropout was then applied to the model to demonstrate how this technique can mitigate overfitting.
  
**How to Run the Code**

  Prerequisites: 🛠️ Make sure you have the necessary libraries, such as PyTorch, installed.
  
  Run the Notebook: 🖥️ The code is available in your_notebook_name.ipynb. You can run it in Google Colab or any Jupyter environment.
  
Niloufar Soleil
