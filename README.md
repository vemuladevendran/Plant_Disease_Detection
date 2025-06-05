# 🌿 Plant Disease Detection Using CNN

This project focuses on detecting plant diseases using a Convolutional Neural Network (CNN) trained on a large dataset of plant images. A basic web interface using Streamlit is also provided for testing predictions with custom images.

---

## 📁 Dataset

- **Source**: [Kaggle - New Plant Diseases Dataset](https://www.kaggle.com/datasets/vipoooool/new-plant-diseases-dataset/data)
- **Description**: Contains approximately **87,000 RGB images** categorized into **33 classes**.
- **Split**:
  - Training: 80%
  - Validation: 20%

---

## 🧹 Data Preprocessing

Used **TensorFlow** to preprocess images for both training and validation datasets:
- Resizing and normalization of image data.
- One-hot encoding of class labels.
- Applied shuffling and batching.

---

## 🧠 Model Architecture: CNN

A **Convolutional Neural Network (CNN)** is used, which is ideal for image classification tasks.

### 🏗 CNN Components:

1. **Input Layer**  
   - Accepts 3D image input (Height × Width × Channels for RGB).

2. **Convolution Layer**  
   - Applies 3×3 or 5×5 filters to extract spatial features.
   - Generates feature maps to detect patterns like edges and textures.

3. **ReLU Activation**  
   - Applies non-linearity with `f(x) = max(0, x)`.

4. **Pooling Layer (e.g., Max Pooling)**  
   - Reduces dimensions (downsampling).
   - Retains significant features (e.g., max value in 2×2 region).

5. **Stacking Layers**  
   - Deeper Conv + Pool layers to extract complex features.

6. **Flattening Layer**  
   - Converts feature maps into a 1D vector.

7. **Fully Connected Layer**  
   - Final layer(s) for learning decision boundaries.
   - Ends with a **Softmax** layer for multi-class classification.

---

## 🌐 Web Interface

Developed a basic **Streamlit** interface:
- Upload an image via the UI.
- Model predicts the class (plant disease type).
- Easy-to-use and accessible for quick testing.

---

## 🚀 How to Run

```bash
# Install dependencies
pip install tensorflow streamlit

# Run the web app
streamlit run main.py
