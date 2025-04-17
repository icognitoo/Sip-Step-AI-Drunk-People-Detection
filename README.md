# 🚶‍♂ Sip-Step-AI-Drunk-People-Detection
A deep learning-based video classification project that detects whether a person is drunk or sober from video footage using a hybrid CNN + LSTM model, with optional frame-level predictions using a lightweight CNN.

📌 Project Overview
Sip-Step-AI-Drunk-People-Detection is an end-to-end system that classifies videos of individuals based on their behavior and movement patterns. It processes video files into TensorFlow TFRecord format, trains a model with spatial and temporal learning components, and provides quick inference through frame-by-frame analysis.

🧠 Core Features
🎞️ Video Preprocessing: Extracts and resizes frames from video clips.

📁 TFRecord Pipeline: Stores processed data efficiently for training and evaluation.

🧬 Model 1 - ResNet50 + LSTM: Learns both visual and temporal features from sequences of frames.

⚡ Model 2 - Frame-Level CNN: Predicts intoxication from individual frames for faster inference.

🛠️ Training Utilities: Checkpointing, early stopping, and backup/restore for stable training.

🧪 Demo Classifier: Includes a simple MNIST classifier for digit recognition.

📂 Folder Structure
graphql
Copy
Edit
├── checkpoints/       # Saved model checkpoints
├── tfrecords/         # TFRecord files for training/testing
├── videos/            # Upload directory for raw video files
├── backup/            # Training recovery snapshots
├── main.py            # End-to-end training and inference script
├── README.md          # Project documentation
⚙️ Requirements
Python 3.8+

TensorFlow 2.x

OpenCV

NumPy

Google Colab (recommended for ease of file upload and GPU usage)

Install with:

bash
Copy
Edit
pip install tensorflow opencv-python numpy
🚀 How to Use
Upload a ZIP of your videos when prompted in Colab.

Videos should be named Drunk*.mp4 or Sober*.mp4.

The code automatically:

Extracts frames,

Converts them into TFRecords,

Trains the LSTM model,

And saves checkpoints.

For quick predictions, use the frame-based model:

python
Copy
Edit
predict_video('path/to/video.mp4')
🧪 Model Outputs
Model 1: Returns a single prediction (Drunk or Sober) for a full video.

Model 2: Averages predictions across frames for faster inference.

📈 Metrics Used
Accuracy

Precision

Recall

🤖 Applications
Public safety

Surveillance analytics

Event monitoring

Automotive in-cabin systems
