# 👕 Fashion MNIST Image Classification using CNN | Deep Learning


## 📌 Project Overview

This project focuses on building a **Convolutional Neural Network (CNN)** using Deep Learning to classify fashion product images into 10 different clothing categories using the Fashion-MNIST dataset.

The model takes a grayscale image of a clothing item as input, processes it through multiple convolutional and pooling layers, and predicts the corresponding clothing category using a Softmax output layer.

The main objective of this project is to understand and implement fundamental Deep Learning concepts, including image preprocessing, convolution operations, feature extraction, Max Pooling, CNN architecture, model training, evaluation, and multi-class image classification.

## 🎯 Project Objectives

- Build an image classification model using CNN.
- Understand how convolutional layers extract image features.
- Implement Max Pooling to reduce spatial dimensions.
- Perform image normalization and preprocessing.
- Train and validate a CNN model.
- Evaluate model performance using different classification metrics.
- Visualize training accuracy and loss.
- Analyze predictions using a confusion matrix and classification report.

## 📊 Dataset Information

**Dataset:** Fashion-MNIST

Fashion-MNIST is a dataset containing grayscale images of fashion products. It consists of 70,000 images divided into 60,000 training images and 10,000 testing images.

Each image has a resolution of 28 × 28 pixels and belongs to one of 10 clothing categories.

### 👗 Dataset Classes

| Label | Clothing Category |
|---|---|
| 0 | T-shirt/top |
| 1 | Trouser |
| 2 | Pullover |
| 3 | Dress |
| 4 | Coat |
| 5 | Sandal |
| 6 | Shirt |
| 7 | Sneaker |
| 8 | Bag |
| 9 | Ankle boot |

### 📦 Dataset Split Used in This Project

Instead of using the entire dataset, this project uses a smaller balanced subset for model training and evaluation.

| Dataset | Number of Images |
|---|---:|
| Training Set | 8,000 |
| Validation Set | 2,000 |
| Testing Set | 2,000 |
| **Total** | **12,000** |

The training and validation sets are selected from the original training dataset, while the testing subset is selected separately from the original test dataset.

The dataset is automatically downloaded through Keras.

## 🛠️ Technologies & Libraries Used

| Technology | Purpose |
|---|---|
| Python | Programming Language |
| NumPy | Numerical computations and array operations |
| Pandas | Prediction probability analysis |
| Matplotlib | Data visualization and plotting |
| Keras | Building and training the CNN model |
| TensorFlow | Deep Learning backend |
| Scikit-learn | Dataset splitting and model evaluation |

### 🧠 Deep Learning Concepts Implemented

- Artificial Neural Networks (ANN) fundamentals
- Convolutional Neural Networks (CNN)
- Convolution Operations
- Feature Extraction
- ReLU Activation Function
- Max Pooling
- Flatten Layer
- Fully Connected (Dense) Layers
- Softmax Activation
- Adam Optimizer
- Sparse Categorical Crossentropy
- Forward Propagation
- Multi-class Image Classification

## 🏗️ CNN Model Architecture

The project uses a Sequential CNN architecture consisting of two convolutional blocks followed by fully connected classification layers.

### Model Architecture

```text
Input Image (28 × 28 × 1)
          |
          v
Conv2D (32 Filters, 3×3)
          |
          v
ReLU Activation
          |
          v
MaxPooling2D (2×2)
          |
          v
Conv2D (64 Filters, 3×3)
          |
          v
ReLU Activation
          |
          v
MaxPooling2D (2×2)
          |
          v
Flatten Layer
          |
          v
Dense Layer (64 Neurons)
          |
          v
ReLU Activation
          |
          v
Output Layer (10 Neurons)
          |
          v
Softmax Activation
          |
          v
Predicted Clothing Category
```

### ⚙️ Model Configuration

| Parameter | Value |
|---|---|
| Input Shape | 28 × 28 × 1 |
| Convolutional Layers | 2 |
| First Conv2D Filters | 32 |
| Second Conv2D Filters | 64 |
| Kernel Size | 3 × 3 |
| Padding | Same |
| Pooling | Max Pooling |
| Pool Size | 2 × 2 |
| Hidden Dense Layer | 64 Neurons |
| Output Neurons | 10 |
| Output Activation | Softmax |
| Hidden Activation | ReLU |

## 🔄 Project Workflow

The complete project follows these steps:

**1. 📥 Dataset Loading**

- Load Fashion-MNIST dataset using Keras.
- Separate training and testing images.
- Define all 10 clothing class names.

**2. 📊 Exploratory Data Analysis**

- Display sample fashion images.
- Inspect image dimensions.
- Check pixel data types.
- Identify minimum and maximum pixel values.
- Visualize image labels.

**3. 🧹 Data Preprocessing**

- Convert image data into Float32.
- Normalize pixel values from 0–255 to 0–1.
- Create a smaller dataset for experimentation.
- Split training data into training and validation sets.
- Select a balanced testing subset.
- Add an extra channel dimension for CNN input.

**4. 🧮 Understanding Convolution**

- Implement a small numerical convolution example.
- Apply an example filter to an image patch.
- Calculate element-wise multiplication and summation.

**5. 🏗️ CNN Model Building**

- Create a Sequential CNN model.
- Add two Conv2D layers.
- Apply ReLU activation.
- Add MaxPooling2D layers.
- Flatten extracted features.
- Add Dense classification layers.
- Generate 10 output probabilities.

**6. ⚙️ Model Compilation**

- Optimizer: Adam
- Learning Rate: 0.001
- Loss Function: Sparse Categorical Crossentropy
- Evaluation Metric: Accuracy

**7. 🚀 Model Training**

- Train the CNN model for 10 epochs.
- Use a batch size of 64.
- Monitor training and validation performance.

**8. 📈 Performance Visualization**

- Plot training accuracy.
- Plot validation accuracy.
- Plot training loss.
- Plot validation loss.

**9. 🧪 Model Evaluation**

- Evaluate the model on the testing dataset.
- Calculate test loss and accuracy.
- Generate predicted class probabilities.
- Identify predicted classes using Argmax.

**10. 📋 Classification Analysis**

- Generate a confusion matrix.
- Generate a classification report.
- Calculate precision, recall and F1-score.
- Compare actual and predicted clothing categories.
- Inspect prediction confidence and class probabilities.

## 📈 Model Evaluation Metrics

The following evaluation techniques are implemented:

| Metric | Description |
|---|---|
| Accuracy | Measures overall correct predictions |
| Loss | Measures prediction error |
| Precision | Measures correctness of positive predictions |
| Recall | Measures how many actual class samples are identified |
| F1-Score | Harmonic mean of precision and recall |
| Confusion Matrix | Visualizes correct and incorrect classifications |

### 📊 Visualizations Included

- Sample Fashion-MNIST Images
- Training vs Validation Accuracy Graph
- Training vs Validation Loss Graph
- Confusion Matrix
- Actual vs Predicted Image Comparison
- Prediction Confidence
- Class-wise Probability Table

**Note:** Actual accuracy, loss, precision, recall and F1-score are generated when the notebook is executed. No unverified performance numbers are reported here.

## 📁 Project Structure

```text
Fashion-MNIST-CNN/
│
├── Fashion_MNIST_CNN_Standalone.ipynb
│
└── README.md
```

## 💻 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/Fashion-MNIST-CNN.git
```

### 2. Navigate to the Project Folder

```bash
cd Fashion-MNIST-CNN
```

### 3. Create a Virtual Environment (Optional)

```bash
python -m venv myenv
```

Activate on Windows:

```bash
myenv\Scripts\activate
```

### 4. Install Required Libraries

```bash
pip install numpy pandas matplotlib scikit-learn tensorflow jupyter
```

### 5. Run Jupyter Notebook

```bash
jupyter notebook
```

Open:

`Fashion_MNIST_CNN_Standalone.ipynb`

Run all notebook cells sequentially.

## 🎯 Project Learning Outcomes

Through this project, I gained practical experience in:

- Understanding the working principles of CNN architectures.
- Performing image preprocessing and normalization.
- Understanding convolution and feature extraction.
- Implementing Max Pooling and Flatten layers.
- Building and training a Deep Learning model using Keras.
- Working with multi-class classification problems.
- Evaluating models using Scikit-learn.
- Visualizing model performance and prediction results.
- Understanding how neural networks classify image data.

## 🔮 Future Improvements

The project can be extended with the following improvements:

- Experiment with deeper CNN architectures.
- Implement Dropout and Batch Normalization.
- Apply Data Augmentation.
- Experiment with different optimizers and learning rates.
- Use the complete Fashion-MNIST dataset.
- Implement Transfer Learning using suitable image models.
- Build an interactive web application using Streamlit.
- Deploy the trained model for real-time image classification.

## 👨‍💻 Author

**Dheeraj Chouhan**

B.Tech – Information Technology

Interested in Artificial Intelligence, Machine Learning, Deep Learning, and Generative AI.

### 🔗 Connect With Me

- GitHub: https://github.com/dheeraj24-coder
- Portfolio: https://dheeraj-chouhan-aiml-engineer-portf.vercel.app/
- Linkdin: https://www.linkedin.com/in/dheeraj-chouhan-7a6996371/

---

⭐ If you find this project useful, don't forget to star the repository!

**Built with ❤️ using Python, Keras, and Deep Learning.**
