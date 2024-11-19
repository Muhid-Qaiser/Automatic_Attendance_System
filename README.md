# README: Automatic Attendence System's Documentation

## Project Overview

An AI powered system that allows teachers to take attendance of all students with a snigle snap of the camera.
This project is a Python-based implementation for detecting and recognizing faces in images. The code is structured in a Jupyter Notebook format, allowing users to execute the steps interactively and visualize outputs. As of now, the code is limited to recognizing faces in a given image without additional features like face identification or classification.

---

## Features and Current Status

### Implemented Features
- **Face Detection**: The code identifies and detects faces in an image.
- **Image Input**: Supports reading and processing images from local storage.
- **Visualization**: Outputs images with detected faces highlighted using bounding boxes.

### Features in Progress
- None at the moment.

### Future Scope
- Face Recognition (matching detected faces with a database).
- Real-time face detection using webcam or video input or image.
- Enhanced accuracy with advanced pre-trained models or fine-tuning.
- Facial Recognition Module which will be implemented using the face_recognition library or siamese neural networks.

---

## File Structure and Code Walkthrough

The notebook contains the following sections:

### 1. **Imports and Setup**
- Imports all required libraries, including `cv2` (OpenCV), `matplotlib` and `RetinaFace` for image processing, visualization and Face Detection.

### 2. **Loading the Image**
- Reads an image file from the local system using OpenCV.
- Converts the image from BGR (default in OpenCV) to RGB for visualization consistency.

### 3. **Face Detection**
- Uses a the pretrained RetinaFace model to detect faces from the loaded image.

### 4. **Storing the Faces**
- Detected faces are extracted and returned as dictionary with keys being 'face_1', 'face_2' ... etc which contain information about different landmarks of each faces.

### 5. **Displaying Image**
- Displays the processed image with  using `matplotlib`.

  
### 6. **Extracting Faces from Image**
- Detected faces are detected and extracted and returned as list of 2D array which signify a face.
- Each face is then displayed using `matplotlib`.

### 7. **Saving the Extraced Faces**
- We use a simple code utilizing the OS library to store all faces in a separate folder in Download Directory

---

## Prerequisites

### Software Requirements
- Python 3.7 or above
- Jupyter Notebook (for running the `.ipynb` file)
- Required libraries:
  - `opencv-python`
  - `matplotlib`
  - `retina-face`

### Installation
Install the required Python packages using the following command:
```bash
pip install opencv-python matplotlib retina-face
```

---

## How to Use

1. **Clone the Repository**
   Download or clone the repository containing the notebook file.

2. **Run the Notebook**
   - Open the notebook in Jupyter Notebook or Jupyter Lab.
   - Execute the cells in sequence.
   - Make sure the input image is available in the specified path.

3. **Provide Input**
   Replace the image path in the `cv2.imread()` function with the desired image file.

4. **View Results**
   The output image with detected faces will be displayed in the notebook.

---

## Limitations
- **Face Detection Only**: The current code only detects faces; it does not identify individuals.
- **Static Images**: Only supports static image inputs; does not handle video or webcam streams.
- **Model Limitations**: Relies on Haar Cascade, which may not perform well in complex scenarios (e.g., varying lighting conditions, occlusions).

---

## Future Improvements
To enhance functionality:
1. Add real-time video feed detection.
2. Extend the code to perform face recognition and matching.

---

## Acknowledgments
The face detection implementation uses RetinaFace's pre-trained model. 

---

## Author
- **Name**: Muhid Qaiser
- **Contact**: i220472@nu.edu.pk

--- 

