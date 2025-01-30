# DeepFakeArt: CNN-Based Forgery Detection
DeepFakeArt: CNN-Based Forgery Detection

**📌 Project Overview**

DeepFakeArt is a Convolutional Neural Network (CNN)-based model designed to detect forged and manipulated images using deep learning techniques. It classifies images as similar or dissimilar based on various forgery methods such as style transfer, inpainting, adversarial attacks, and CutMix augmentation.

**🚀 Features**

* Forgery Detection: Identifies whether two images are similar (forged) or dissimilar (not related).
* Deep Learning with CNN: Uses Conv2D, MaxPooling, Dense, and Dropout layers for classification.
- Multiple Forgery Techniques: Detects inpainting, style transfer, adversarial manipulation, and more.
-Dataset Handling: Automatically loads and processes the Kaggle dataset deepfakeart.
- Google Colab Support: Train and test the model on Colab with minimal setup.

**📂 Dataset Structure**

The dataset follows this structure:
```
/content/deepfakeart/
│── dissimilar/
│   ├── test_dissimilar.json
│   ├── train_dissimilar.json
│
│── similar/
│   ├── adversarial/
│   │   ├── 0, 1, 2... (folders with original + altered images)
│   ├── cutmix/
│   ├── inpainting/
│   │   ├── group.png, inpainting.png, mask.png, original.png
│   ├── style_transfer/
│   │   ├── test_similar.json, train_similar.json
```

**🔧 Installation & Setup**

- Step 1️⃣: Clone the Repository
```
git clone https://github.com/yourusername/deepfakeart.git
cd deepfakeart
```

- Step 2️⃣: Install Dependencies
```
pip install -r requirements.txt
```
(Ensure TensorFlow, Keras, NumPy, and OpenCV are installed)

- Step 3️⃣: Download Kaggle Dataset
**🔹 Get Kaggle API Key (kaggle.json)**
> Go to Kaggle and log in.
> Click on your profile picture > Account.
> Scroll down to the API section.
> Click Create New API Token (A kaggle.json file will download).
🔹 Upload kaggle.json to Google Colab
```
from google.colab import files
files.upload()  # Select kaggle.json from your device
```
🔹 Move kaggle.json to Correct Directory
```
mkdir -p ~/.kaggle
mv kaggle.json ~/.kaggle/
chmod 600 ~/.kaggle/kaggle.json
```
🔹 Download Dataset
```
kaggle datasets download -d dataset-owner/deepfakeart -p /content/deepfakeart --unzip
```

**📜 Usage**
- Train the Model
```
python train.py
```
- Test on Random Image Pairs
```
test_random_pairs.py
```
- Run on Google Colab
- Upload and run the provided deepfakeart_colab.ipynb notebook.

**📊 Results & Performance**
- Achieved XX% accuracy on test data.
- Successfully detected forged images across various manipulation techniques.

🌟 If you like this project, give it a ⭐ on GitHub!

