# Expression Detection

This project focuses on facial expression detection using a Convolutional Neural Network (CNN) implemented in Keras. The model is designed to recognize emotions such as anger, fear, happiness, neutrality, sadness, and surprise based on facial expressions.

## Technologies Used

- Keras
- OpenCV
- NumPy
- Python

## Project Structure

The project is organized into the following components:

### 1. Model Definition

The CNN model is defined using Keras, with layers for convolution, batch normalization, max-pooling, dropout, and dense layers for classification. The architecture is summarized using `model.summary()`.

### 2. Image Data Handling

ImageDataGenerator is employed to augment training data and normalize pixel values. The data is divided into training and validation sets.

### 3. Model Training

The model is compiled using categorical crossentropy loss and the Adam optimizer with a small learning rate. Training is performed using a generator to handle the large image dataset.

### 4. Model Evaluation

Callbacks such as ModelCheckpoint, EarlyStopping, and ReduceLROnPlateau are utilized during training. The final trained model is saved as 'emotion3.h5'.

### 5. Real-time Emotion Detection

A real-time emotion detection script captures video frames using OpenCV, detects faces, preprocesses the images, and predicts emotions using the trained model. Detected emotions are overlayed on the video feed.

## How to Use

1. Clone the repository.
2. Install the required dependencies: `keras`, `opencv`, `numpy`.
3. Run the real-time emotion detection script: `python real_time_emotion_detection.py`.

Note: Ensure the pre-trained model file 'emotion3.h5' is available in the project directory.

Feel free to experiment with the model and enhance its capabilities for more accurate emotion detection.
