# Object Detection Using Shape-based Matching

## Overview
This project performs object detection using shape-based template matching in images. The approach involves preprocessing the images, extracting edges, identifying object contours, and matching templates using OpenCV functions. The process does not rely on deep learning but rather traditional computer vision techniques.

## Requirements
Ensure you have the following dependencies installed before running the code:
```bash
pip install opencv-python numpy matplotlib
```

## Workflow
### 1. Load and Preprocess Images
- Read the input image (`finding.jpg`) and convert it to RGB format.
- Split the image into two parts: the main image and the template.
- Convert both parts to grayscale and apply Gaussian blur.
- Perform edge detection using Canny edge detector.

### 2. Save Processed Images
- Save the main and template images to the `analyst/` directory.
- Convert the template image to binary format and extract contours.

### 3. Extract Objects from Template
- Find contours of objects in the template image.
- Extract object bounding boxes and save them in the `extracted_objects/` directory.

### 4. Template Matching
- Iterate through different scale values and apply template matching.
- Identify the best location and scale factor for the match.
- Draw a bounding box around the detected object in the main image.

## Running the Code
1. Ensure all images are present in the working directory.

2. Run the script in a Jupyter Notebook or as a standalone Python script.

3. The extracted objects will be saved in `extracted_objects/`.

4. The final detection result will be displayed using Matplotlib.

## Expected Output

<table>
  <tr>
    <th>Result_1</th>
    <th>Result_2</th>
  </tr>
  <tr>
    <td><img src="output_1.png" width="300"></td>
    <td><img src="output_2.png" width="300"></td>
  </tr>
</table>
