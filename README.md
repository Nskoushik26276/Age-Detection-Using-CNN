# 🧠 Age Group Detection using CNN & Transfer Learning

A deep learning project that predicts a person's age group (e.g., 0–10, 11–20, etc.) from a single face photo.  
Built using transfer learning with MobileNetV2, data augmentation, and fine-tuning to achieve better accuracy even on imbalanced age datasets.

---

## ✨ **Features**
✅ Predict age group from photo (7 age buckets)  
✅ Transfer learning with pretrained MobileNetV2  
✅ Fine-tuning last layers for better generalization  
✅ Handles imbalanced classes using data augmentation  
✅ Runs on Google Colab (with GPU) or Jupyter Notebook locally

---

## ⚙️ **How it works**
1. Dataset (UTKFace) contains face images labeled with age in filename.
2. Images are resized & normalized.
3. Ages are converted into 7 buckets:
   - `0–10`, `11–20`, `21–30`, `31–40`, `41–50`, `51–60`, `61+`
4. Pretrained MobileNetV2 (trained on ImageNet) is used:
   - Last 30 layers are unfrozen & fine-tuned on our dataset.
5. Trained model predicts the most probable age bucket for new images.

---

## 🚀 **Getting started**

### ✅ Clone / Download the project
```bash
git clone https://github.com/yourusername/age-detection-cnn.git
cd age-detection-cnn
✅ Download dataset (UTKFace)
Option 1: Using Kaggle
Place your kaggle.json in root folder (get it from Kaggle API)

bash
Copy
Edit
pip install kaggle
kaggle datasets download -d vivekprasadkushwaha/utkface
unzip utkface.zip -d dataset
Option 2: Download manually
Download from: https://www.kaggle.com/datasets/vivekprasadkushwaha/utkface

Extract images to dataset/ folder

🧰 Install dependencies
bash
Copy
Edit
pip install tensorflow keras scikit-learn opencv-python matplotlib
🧪 Run the notebook
In Jupyter Notebook:

bash
Copy
Edit
jupyter notebook age_detection.ipynb
Or run in Google Colab (recommended for GPU):

Upload notebook to Colab

Run each cell step by step

📷 Predict age group from new photo
Upload any photo in notebook:

It resizes & preprocesses the image

Model predicts the most probable age bucket
Example:

python
Copy
Edit
🎉 Predicted age group: 21–30
📦 Technologies used
Python, NumPy, OpenCV, scikit-learn

TensorFlow, Keras

MobileNetV2 pretrained on ImageNet

UTKFace dataset

Google Colab (for GPU training)

