# THRESHOLDING
## NAME : SRI HARI KRISHNA D T
## REG NO : 212224240160
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm

### Step1:
Load the necessary packages

### Step2:
Read the Image and convert to grayscale
### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.

## Program


# Load the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

```

# Read the Image and convert to grayscale
```
image = cv2.imread("C:\\Users\\admin\\Downloads\\My image.png")  
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)  

```



# Convert from BGR to RGB for display
```
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Original Image")
plt.axis('off')
```
# Use Global thresholding to segment the image
```
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)

```

# Use Adaptive thresholding to segment the image

```
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)


```


# Use Otsu's method to segment the image 
```
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

```



# Display the results

# Global Thresholding
```
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```
# Adaptive Thresholding
```
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
# Otsu's Method
```
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')
```
# Show the plot
```
plt.tight_layout()
plt.show()
<img width="437" height="370" alt="Screenshot 2026-05-23 182646" src="https://github.com/user-attachments/assets/6742e318-0f95-47f5-aab9-b6b76e87abbc" />

```


## Output

### Original Image

<img width="761" height="383" alt="image" src="https://github.com/user-attachments/assets/c6dfacd5-fe6b-413b-aba5-b267aa4e50b2" />


### Global Thresholding

<img width="716" height="673" alt="image" src="https://github.com/user-attachments/assets/fbb7529c-8ffd-435a-8548-ef863147b587" />

### Adaptive Thresholding

<img width="716" height="673" alt="image" src="https://github.com/user-attachments/assets/ec39235c-bf89-4b1e-ad57-4d55bb952d96" />


## Optimum Global Thesholding using Otsu's Method

<img width="716" height="673" alt="image" src="https://github.com/user-attachments/assets/abe4188f-9b56-4872-8cb3-e86e58d24b18" />


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
