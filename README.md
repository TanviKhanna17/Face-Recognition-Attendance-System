# Face Recognition Attendance System

This project implements a real-time face recognition attendance system using OpenCV and machine learning techniques. It captures video from a webcam, detects faces, recognizes individuals, and logs attendance with timestamps.

## Features

- Real-time face detection and recognition
- Attendance logging with date and time
- User-friendly interface with visual feedback
- CSV-based attendance record storage

## Requirements

- Python 3.x
- OpenCV
- scikit-learn
- NumPy

## Installation

1. Clone this repository:
   git clone https://github.com/your-username/face-recognition-attendance-system.git
2. Install the required packages:
   pip install opencv-python scikit-learn numpy
3. Download the Haar Cascade classifier XML file and place it in the `Data` directory.

## Usage

1. Prepare your dataset:
- Collect face images of individuals to be recognized
- Train the model and save the data using the provided scripts : python add_faces.py

2. Run the main script: python test.py
3. The system will start capturing video from your webcam and recognizing faces.

4. Press 'o' to log attendance for the recognized individual.

5. Press 'q' to quit the application.

## How it works

1. The system uses a pre-trained Haar Cascade classifier to detect faces in the video stream.
2. Detected faces are cropped, resized, and flattened into a 1D array.
3. A K-Nearest Neighbors (KNN) classifier predicts the identity of the face.
4. The recognized name is displayed on the video feed in real-time.
5. When logging attendance, the system saves the name and timestamp to a CSV file.

## Customization

- Adjust the `n_neighbors` parameter in the KNN classifier for different accuracy levels.
- Modify the face detection parameters in `facedetect.detectMultiScale()` for better face detection in different environments.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).

