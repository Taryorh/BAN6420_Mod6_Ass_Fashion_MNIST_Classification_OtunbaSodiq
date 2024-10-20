# BAN6420_Mod6_Ass_Fashion_MNIST_Classification_OtunbaSodiq
This is my submission for Assignment Module 6 "Fashion MNIST Classification" - Sodiq Otunba Learner ID 154046

# Fashion MNIST Classification using Deep Learning in Python and R
This repository contains two implementations (in Python and R) of a deep learning model to classify images from the Fashion MNIST dataset. Both implementations use the Keras library for building and training the model. The goal is to correctly classify clothing images into one of 10 categories.

# Overview
This project demonstrates the use of deep learning to classify images from the Fashion MNIST dataset. Implementations are provided in both Python and R, allowing users to explore the similarities and differences between the two languages for deep learning tasks using the Keras API.

# Dataset
The Fashion MNIST dataset consists of 70,000 grayscale images of clothing, with 10 classes including:

- T-shirt/top

- Trouser

- Pullover

- Dress

- Coat

- Sandal

- Shirt

- Sneaker

- Bag

- Ankle boot

- Training Set: 60,000 images

- Test Set: 10,000 images

# Model Architecture
Both the Python and R versions use the same architecture for the model, which includes:

- Input Layer: A 28x28 grayscale image.
- Flatten Layer: Converts the 2D image into a 1D vector.
- Dense Layer: A fully connected layer with 128 units and ReLU activation.
- Dropout Layer: A dropout rate of 0.2 for regularization.
- Output Layer: A dense layer with 10 units for the 10 categories, using softmax activation.
The model structure is the same in both implementations.

Python Model 

```bash
model = keras.Sequential([
    keras.layers.Flatten(input_shape=(28, 28)),
    keras.layers.Dense(128, activation='relu'),
    keras.layers.Dropout(0.2),
    keras.layers.Dense(10, activation='softmax')
])
```
```R
model <- keras_model_sequential() %>%
  layer_flatten(input_shape = c(28, 28)) %>%
  layer_dense(units = 128, activation = 'relu') %>%
  layer_dropout(rate = 0.2) %>%
  layer_dense(units = 10, activation = 'softmax')
```

# Results
Both the Python and R implementations should produce similar results, with accuracy on the test set around 87-89% for 5 epochs of training.
