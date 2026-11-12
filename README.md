# EXP.3-Record-Histogram-Processing
# Histogram Equalization Using OpenCV (Grayscale & Color Images)

# Aim
To write a Python program using OpenCV to perform histogram equalization on both grayscale and color images to enhance image contrast and brightness.

The program performs the following operations:

Read and display a grayscale image
Plot histogram of the grayscale image
Apply histogram equalization on grayscale image
Read and display a color image
Plot histogram of B, G, R channels
Convert image to HSV color space
Apply histogram equalization on the Value (V) channel
Convert the enhanced image back to BGR format
Display original and enhanced images with histograms
# Software Used
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib
# Algorithm
Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

Step 2:
Read the image parrot.jpg in grayscale format.

Step 3:
Display the grayscale image and plot its histogram.

Step 4:
Apply histogram equalization using cv2.equalizeHist() to enhance contrast.

Step 5:
Display original grayscale image, its histogram, enhanced image, and its histogram using a 2 × 2 grid.

Step 6:
Read the same image in color format.

Step 7:
Split the image into B, G, R channels and plot their histograms.

Step 8:
Convert the image from BGR to HSV color space.

Step 9:
Apply histogram equalization on the V (Value) channel.

Step 10:
Merge the channels and convert the image back to BGR format.

Step 11:
Display original color image, histogram, enhanced image, and enhanced histogram using a 2 × 2 grid.

# Program Developed By:
# Name: Harini V K
# Register Number: 212225220036
# Program
```
Import Python necessary libraries

import cv2
import numpy as np
import matplotlib.pyplot as plt
Histogram Equalization for Grayscale Images

img = cv2.imread('Harini.new.jpeg', 0)

plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.show()
plt.hist(img.ravel(),256,range = [0, 256]);
plt.title('Original Image')
plt.show()
img_eq = cv2.equalizeHist(img)
plt.hist(img_eq.ravel(), 256, range = [0, 256])
plt.title('Equalized Histogram')
plt.imshow(img_eq, cmap='gray')
plt.title('Original Image')
plt.show()
img = cv2.imread('Harini.new.jpeg', cv2.IMREAD_COLOR)
img_hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
img_hsv[:,:,2] = cv2.equalizeHist(img_hsv[:, :, 2])
img_eq = cv2.cvtColor(img_hsv, cv2.COLOR_HSV2BGR)
plt.imshow(img_eq[:,:,::-1]); plt.title('Equalized Image');plt.show()
plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized');plt.show()
plt.figure(figsize = (20,10))
plt.subplot(221); plt.imshow(img[:, :, ::-1]); plt.title('Original Color Image')
plt.subplot(222); plt.imshow(img_eq[:, :, ::-1]); plt.title('Equalized Image')
plt.show()
plt.figure(figsize = [15,4])
plt.subplot(121); plt.hist(img.ravel(),256,range = [0, 256]); plt.title('Original Image')
plt.subplot(122); plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized')
```
# Output:

<img width="658" height="480" alt="image" src="https://github.com/user-attachments/assets/9c9d0ccf-5629-4d91-947d-ba352cde2a0b" />

<img width="735" height="533" alt="image" src="https://github.com/user-attachments/assets/06d0e515-1b50-4a2a-8702-b682dbc33b38" />

<img width="783" height="535" alt="image" src="https://github.com/user-attachments/assets/159569d8-720f-4143-b84b-ed6629a45f3c" />

<img width="752" height="508" alt="image" src="https://github.com/user-attachments/assets/6a8b17db-bcc9-4e2a-a680-0ec226c6ae20" />

<img width="725" height="482" alt="image" src="https://github.com/user-attachments/assets/54c33c0d-3120-4e2b-a768-3778d0ed8e0f" />

<img width="782" height="537" alt="image" src="https://github.com/user-attachments/assets/909b2439-28e5-4bbf-aaf9-1fa6fc9b30ed" />

<img width="1291" height="372" alt="image" src="https://github.com/user-attachments/assets/c1def421-186b-4166-b9fa-51dea4eb5425" />

<img width="1242" height="363" alt="image" src="https://github.com/user-attachments/assets/e0113d3f-164b-425e-93e1-40ec4968e4be" />


# Result:
Thus, histogram equalization is successfully performed on both grayscale and color images using OpenCV. The contrast and brightness of the images are significantly improved, enhancing visual quality and feature visibility.




