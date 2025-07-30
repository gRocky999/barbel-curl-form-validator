# 💪 Bicep Curl Form Analysis using Mediapipe and Deep Learning

This project analyzes the correctness of **Barbell Bicep Curl** exercise form using **Mediapipe pose estimation** and a **deep learning classification model**.

---

## Features

- ✅ Detects **correct** vs **incorrect** barbell curl forms.
- 🧠 Uses **Mediapipe** to extract pose keypoints and a **custom-trained neural network** for classification.
- 📈 Preprocessing includes **MinMax scaling**, **keypoint normalization**, and **augmentation**.
- 📁 Organized dataset of manually labeled **correct/incorrect form videos**.
- 📊 Detailed metrics and model evaluation.

---

## Technologies Used

- **Python**
- **OpenCV**
- **Mediapipe** (Pose estimation)
- **TensorFlow / Keras** (Neural Network)
- **Scikit-learn** (Scaling, Metrics)
- **Matplotlib / Seaborn** (Visualization)
- **NumPy, Pandas**

---


---

##  How It Works

### 1. **Data Collection & Augmentation**
- Collected 15 videos each of **correct** and **incorrect** bicep curls.
- Applied filters like:
  - Brightness/contrast adjustment
  - Gaussian noise
  - Gaussian/Laplacian blurs
- Saved augmented videos into respective class folders.

### 2. **Pose Estimation**
- Used **Mediapipe** to extract 33 keypoints (x, y, z, visibility) per frame.
- Stored extracted keypoints into CSVs for training.

### 3. **Data Preprocessing**
- Applied **MinMax scaling** on all keypoints using precomputed scaler.
- Balanced dataset with correct/incorrect samples.
- Shuffled and split into train/test sets.

### 4. **Model Training**
- Simple **Dense Neural Network** trained on scaled pose keypoints.
- Binary classification: `Correct (1)` or `Incorrect (0)`
- Evaluated using **accuracy, precision, recall, F1-score**.

### 5. **Real-Time Inference**
- Captures webcam stream, extracts keypoints, scales them, and classifies using saved model.
- Displays result overlay on the video: ✅ Correct or ❌ Incorrect.


---




