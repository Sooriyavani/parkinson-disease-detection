# parkinson-disease-detection
🧠 Parkinson's Disease Detection Using MRI Scans

This is a small project I worked on to understand how deep learning can help in detecting Parkinson’s disease from MRI brain scans. I wanted to make it simple, understandable, and something that could be used through a basic web browser.

🔍 Model Details — What I Used & Why 🔧 Model Architecture I used a Convolutional Neural Network (CNN) — a type of deep learning model that works really well with images. Here's why I chose it:

CNNs are great at finding patterns in images (like edges, textures, and shapes) They can learn complex medical features from MRI scans They don't need you to manually tell them what to look for — they figure it out from the data!

Here’s the architecture I used: Conv2D(32 filters, 3x3) ➝ ReLU ➝ MaxPooling
Conv2D(64 filters, 3x3) ➝ ReLU ➝ MaxPooling
Flatten ➝ Dense(128 units) ➝ ReLU
Dense(3 units for 3 stages) ➝ Softmax

The final layer has 3 neurons that represent:

0 → Early Stage 1 → Moderate Stage 2 → Advanced Stage

📁 Dataset I used a publicly available MRI dataset with labeled images. The dataset is divided into:

Normal (no Parkinson’s)

Parkinson's (with early, moderate, or advanced stage labels)

I preprocessed the images: Resized them to 224x224 Normalized the pixel values Augmented data (flips, zooms) to improve learning

🎯 Model Training Loss Function: Categorical Crossentropy (since it's a multi-class problem) Optimizer: Adam Metrics: Accuracy Epochs: 20 Validation Split: 20% I trained the model in Jupyter Notebook and saved the .h5 file (model weights) after getting decent accuracy.

🧠 Prediction Logic Once the model gives a stage:

If it's Early Stage, it recommends lifestyle changes and mild meds like Selegiline For Moderate, it suggests Levodopa or Dopamine agonists For Advanced, it recommends stronger drugs and consult with a neurologist Note: These are just sample outputs for learning and not real medical advice.


🌱 What I Learned How to build a CNN model for image classification Understanding MRI data and preprocessing steps How to serve a machine learning model with Flask Giving real-world context by suggesting medication based on prediction Importance of responsible AI (I clearly mention it’s for learning, not diagnosis)

