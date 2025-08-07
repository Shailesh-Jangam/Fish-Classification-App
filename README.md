
# 🐠 Fish Species Image Classifier with DenseNet121

This project is a deep learning-based image classification app that identifies 11 different fish species using Convolutional Neural Networks (CNNs) and transfer learning (DenseNet121). The model is deployed as a web application using **Streamlit**.

---

## 📌 Project Overview

- 🎯 **Goal**: Predict fish species from images with high accuracy
- 🧠 **Model**: DenseNet121 (pretrained on ImageNet)
- 📷 **Data**: 11 fish categories, ~9.5k images (train/val/test)
- 🌐 **Deployment**: Streamlit web app for real-time image classification

---

## 🗂️ Dataset Structure

```
Dataset/
├── train/
│   ├── class_1/
│   ├── class_2/
│   └── ...
├── val/
├── test/
```

- Total classes: 11 (e.g., trout, shrimp, red_mullet, etc.)
- Imbalanced: One class had very few samples (`animal fish bass`)

---

## 🏗️ Project Structure

```
fish_classifier_app/
├── app.py                 # Streamlit app
├── densenet_model.h5      # Trained model
├── requirements.txt       # Project dependencies
└── README.md
```

---

## 🔍 Model Summary

| Model        | Accuracy | Notes                             |
|--------------|----------|-----------------------------------|
| Custom CNN   | 97%      | Good performance                  |
| VGG16        | 95%      | Solid baseline                    |
| ResNet50     | 31%      | Overfit or failed to converge     |
| EfficientNet | 16%      | Very Low                         |
| ✅ DenseNet121 | 98%      | Final model used for deployment   |

---

## 📊 Final Performance (DenseNet121)

- ✅ **Accuracy**: 98%
- 📈 High F1-score across almost all classes
- ⚠️ Still struggles with the rare class: `animal fish bass`

---

## 🚀 Run the App Locally

### 2️⃣ Install Dependencies
```bash (prpmpt)
pip install -r requirements.txt
```

### 3️⃣ Run the App
```bash (prompt)
streamlit run app.py
```

---

## 🖼️ Example Output

- Upload a fish image
- Get predicted class + confidence score
- Image preview with label

---

## 📦 Requirements

```
tensorflow
keras
streamlit
numpy
opencv-python
pillow
scikit-learn
matplotlib
```

---

## 👨‍💻 Author

**Shailesh Jangam**  
🔗 [LinkedIn](https://linkedin.com/in/shailesh-jangam)  
💻 [GitHub](https://github.com/shailesh-jangam)

---

## ⭐️ Acknowledgements

- Transfer learning with DenseNet121 via Keras
- Inspired by real-world fish classification challenges
- Thanks to LabMentix, the dataset providers
