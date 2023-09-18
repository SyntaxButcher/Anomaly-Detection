# Washer Anomaly Detection
Anomaly detection is a critical application in many industries, from fraud detection to network security. In this project, we focus on detecting anomalies in washers using deep learning.

## Objective
To develop a deep learning model that can identify anomalies in washers by analyzing images. The model is trained on images of conforming washers and is then used to detect non-conforming or anomalous washers.

## Methodology

**Data Collection and Preprocessing:**
Images of conforming washers were collected and stored in the data/train/conform directory.
Images were loaded and preprocessed using OpenCV.
The images were normalized and reshaped to be fed into the neural network.

**Model Architecture:**
We used an autoencoder architecture, a type of neural network that is trained to reproduce its input.
The encoder compresses the input into a latent-space representation, and the decoder then reconstructs the input data from this representation.
The idea is that anomalies will have a higher reconstruction error.

**Training:**
The model was trained using the Mean Squared Error (MSE) loss function.
Adam optimizer was used with a learning rate of 0.0001.
Early stopping was implemented to prevent overfitting.

**Evaluation:**
A threshold for anomaly detection was set using the 99th percentile of the reconstruction error on the training data.
The model's performance was evaluated on a separate test dataset.
Metrics such as accuracy, precision, recall, and F1 score were computed.

**Visualization:**
Original and reconstructed images were visualized to inspect the model's performance.
A confusion matrix was plotted to get a clear view of the model's predictions.

## Results
The model achieved an accuracy of 85.5% on the test dataset with a precision of 98.63%. The recall was 72%, and the F1 score was 83.24%.
