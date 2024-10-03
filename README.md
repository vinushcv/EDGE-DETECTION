# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import all the necessary modules for the program.

### Step 2:
Load a image using imread() from cv2 module.

### Step 3:
Convert the image to grayscale

### Step 4:
Using Sobel operator from cv2,detect the edges of the image.

### Step 5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
```
Developed By: Vinush.CV
Register No: 212222230176
```
```python
# Import necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('badminton.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
### ORIGINAL IMAGE 

![image](https://github.com/user-attachments/assets/53003f4e-f246-4706-ae95-a783c78b58a7)


### SOBEL EDGE DETECTOR
```python
# Apply Sobel edge detector
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
```
![image](https://github.com/user-attachments/assets/a08b175c-20b4-4316-acac-f7928ba122ca)


### LAPLACIAN EDGE DETECTOR
```python
# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
```

![image](https://github.com/user-attachments/assets/b6ecbf92-fe51-457f-b02b-2f6a3abe2c6a)

### CANNY EDGE DETECTOR
```python
# Apply Canny edge detector
canny_edges = cv2.Canny(gray_image, 50, 150)
```


![image](https://github.com/user-attachments/assets/2d5bba6f-fa9a-4fb2-b782-19595fdf457d)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
