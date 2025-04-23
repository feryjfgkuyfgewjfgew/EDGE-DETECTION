# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Output:
### SOBEL EDGE DETECTOR
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('download (1).jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=3)  
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=3)  
sobel_edge = cv2.magnitude(sobel_x, sobel_y)

laplacian_edge = cv2.Laplacian(gray_image, cv2.CV_64F)

canny_edge = cv2.Canny(gray_image, 100, 200)

sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=3)
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=3)

sobel_edge = cv2.magnitude(sobel_x, sobel_y)

sobel_edge = cv2.convertScaleAbs(sobel_edge)

plt.figure(figsize=(8, 6))

plt.subplot(2, 2, 1)
plt.imshow(laplacian_edge, cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis('off')

plt.subplot(2, 2, 2)
plt.imshow(canny_edge, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off')

plt.subplot(2, 2, 3)
plt.imshow(sobel_edge, cmap='gray')  
plt.title("Sobel Edge Detector")
plt.axis('off')

plt.tight_layout()
plt.show()
```

### LAPLACIAN EDGE DETECTOR

![image](https://github.com/user-attachments/assets/22a57fd9-b1c7-4cbd-906b-83582cd6f9f7)



### CANNY EDGE DETECTOR

![image](https://github.com/user-attachments/assets/0eba188b-c56c-4998-a6c7-f271795067ca)

### SOBEL EDGE DETECTOR

![image](https://github.com/user-attachments/assets/d7263a51-36dc-4ad0-a373-345859cdbf9d)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
