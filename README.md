# Handwritten Character Classification using EMNIST  

## Project Information  
- **Assignment-1** Handwritten Character Classification using EMNIST  
- **Student Name:** Ganesh  
- **Roll Number:** 160122737176  
- **Institution:** Chaitanya Bharathi Institute of Technology (CBIT)  
- **Course:** Deep Learning 

## Project Overview  
This project focuses on handwritten character classification using the **EMNIST (Extended MNIST) Balanced dataset**. The task is to compare different optimization techniques—**SGD, Adam, RMSprop, Adagrad and Adadelta**—to determine which optimizer performs the best in training a neural network for image recognition. The assignment involves evaluating the impact of optimizers on training and validation accuracy by varying batch sizes.  

## Dataset Details  
The **EMNIST Balanced dataset** is used, which contains:  
- **Total Classes:** 47 (letters and digits)  
- **Training Images:** 131,600  
- **Testing Images:** 18,800  
- **Image Size:** 28x28 grayscale  

## Model Architecture  
The neural network model consists of:  
- **Input Layer:** 28x28 pixels, flattened into 784 neurons  
- **Hidden Layer 1:** 128 neurons with ReLU activation  
- **Hidden Layer 2:** 64 neurons with ReLU activation  
- **Output Layer:** 47 neurons with Softmax activation  
- **Loss Function:** Categorical Crossentropy  

The model is trained using different batch sizes and optimizers to analyze their impact on accuracy.  

## Optimizer Comparison  
The table below presents the accuracy results for different optimizers:  

| Optimizer  | Batch Size | Training Accuracy | Validation Accuracy |
|------------|------------|-------------------|---------------------|
| SGD        | 128        | 52%               | 50%                 |
| SGD        | 64         | 60%               | 58%                 |
| Adam       | 128        | 80%               | 79%                 |
| Adam       | 64         | 81%               | 80%                 |
| RMSprop    | 128        | 82%               | 81%                 |
| RMSprop    | 64         | 82%               | 81%                 |
| Adadelta   | 128        | 30%               | 28%                 |

## Observations  
- **Adam and RMSprop** provide the best accuracy, making them suitable for handwritten character classification.  
- **SGD** performs moderately well but requires tuning for better results.  
- **Adadelta** shows significantly lower accuracy and is not suitable for this task.  

-The reasons for Low Accuracy:

->**Complex Dataset**: EMNIST has 47 classes (A-Z, a-z, 0-9), making it more challenging. A simple feedforward network may not be powerful enough.

->**Preprocessing Issues**: The EMNIST dataset consists of handwritten characters, which means proper data augmentation (like normalization, rotation, or noise reduction) might help.
Neural Network Architecture: The current architecture is relatively shallow. Adding more hidden layers or using CNNs instead of a simple feedforward network would likely imporve the accuracy.

-The improvement that can be done is switch to a CNN-based model (like LeNet or a simple CNN with Conv2D layers)—Feedforward networks aren't great for image recognition.
