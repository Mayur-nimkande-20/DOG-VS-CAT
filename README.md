# Dog-vs-Cat Classifier using CNN

## Project Overview

This project focuses on building a **Dog-vs-Cat Image Classifier** using a **Convolutional Neural Network (CNN)**. The goal is to classify images of dogs and cats into their respective categories. The CNN model developed for this task consists of three convolutional layers with varying filter sizes (32, 64, and 128). During training, the model encountered an issue of **overfitting**, which was addressed using a suitable technique to improve the model's performance and generalization.

## Model Architecture

The CNN model is designed with the following layers:

1. **Conv2D Layer 1:** 
   - Filters: 32
   - Kernel size: (3x3)
   - Activation: ReLU
   - MaxPooling2D: (2x2)
   
2. **Conv2D Layer 2:** 
   - Filters: 64
   - Kernel size: (3x3)
   - Activation: ReLU
   - MaxPooling2D: (2x2)

3. **Conv2D Layer 3:** 
   - Filters: 128
   - Kernel size: (3x3)
   - Activation: ReLU
   - MaxPooling2D: (2x2)
   
4. **Flatten Layer:** Converts the 2D feature maps into a 1D feature vector.

5. **Fully Connected Layer:** A dense layer with 128 units and ReLU activation.

6. **Output Layer:** A dense layer with 1 unit and sigmoid activation for binary classification (dog vs. cat).

## Overfitting Issue

During training, the model showed high accuracy on the training data but significantly lower accuracy on the validation data. This indicated that the model was **overfitting**, meaning it was memorizing the training data instead of learning general patterns that could be applied to unseen data.

### Overfitting Solutions

To address overfitting, one or more of the following techniques were applied:

- **Dropout:** Dropout layers were added to the fully connected layer to randomly drop neurons during training, preventing the network from becoming too reliant on specific paths.
- **Data Augmentation:** Techniques such as rotating, flipping, and zooming the training images were used to increase the variability in the training data, helping the model generalize better to unseen data.
- **Early Stopping:** Early stopping was implemented to halt training when the model’s performance on the validation set stopped improving, thus preventing overfitting.

These techniques successfully improved the model's generalization and reduced overfitting.

## Results

After applying the selected solution to mitigate overfitting, the model’s performance improved significantly. The validation accuracy increased, and the model was able to generalize better on unseen data.

## Requirements

The following libraries are required to run the project:

- TensorFlow
- Keras
- NumPy
- Matplotlib

To install the necessary libraries, run the following command:
```bash
pip install tensorflow keras numpy matplotlib
```

## Conclusion

This project successfully developed a CNN-based Dog-vs-Cat classifier using three convolutional layers. The initial issue of overfitting was resolved through the application of **Dropout**, **Data Augmentation**, and **Early Stopping**, leading to a more robust and generalizable model.
