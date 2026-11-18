## Record-EDGE-DETECTION

## Exp: No: 6: Edge-detection-opencv

## Aim:
To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

## Software Required:
* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

## ⚙️ Algorithm:

## Step 1:
Import all the necessary modules for the program.

## Step 2:
Load an image using cv2.imread().

## Step 3:
Convert the image to grayscale.

## Step 4:
Apply Sobel operator using OpenCV to detect edges.

## Step 5:
Apply Prewitt operator using custom kernels.

## Step 6:
Apply Roberts operator using custom kernels.

## Step 7:
Apply Laplacian operator using OpenCV.

## Step 8:
Apply Canny edge detector using OpenCV.

## Step 9:
Display all edge-detected images for comparison.

## Program:

## Developed By: SARAN RAJ M

## Register No: 212225240138

## Original Image:

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('sai1.jpeg') 
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

## Sobel Edge Detection:

```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y) 
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```

## Laplacian Edge Detection:

```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```

## Canny Edge Detection:

```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```


## Output:

## Original Image:

<img width="438" height="317" alt="image" src="https://github.com/user-attachments/assets/bc0906ea-550a-4a3e-b20d-07d5e197df0e" />


## Sobel Edge Detection:

<img width="450" height="322" alt="image" src="https://github.com/user-attachments/assets/f95ee074-3149-4277-ae9e-29ba68343f6f" />


## Laplacian Edge Detection:

<img width="487" height="327" alt="image" src="https://github.com/user-attachments/assets/ece5440c-1940-45af-af94-5f0bc35d12e0" />


## Canny Edge Detection:

<img width="431" height="321" alt="image" src="https://github.com/user-attachments/assets/52d44316-42cc-4415-b0ad-4f2418d07613" />


## Result:
Thus, edges are successfully detected using Sobel, Laplacian, and Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.
