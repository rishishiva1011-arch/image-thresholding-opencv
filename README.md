# Image Segmentation Using Thresholding Techniques in OpenCV

## Aim

To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

- Global Thresholding
- Adaptive Thresholding
- Otsu's Thresholding

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

### Original Grayscale Image

- The grayscale version of the input image is displayed.
- Serves as the input for thresholding operations.

### Global Thresholding

- Original image is displayed.
- Thresholded image is displayed.
- A fixed threshold value is used for segmentation.
- Pixels are classified as foreground or background.

### Adaptive Thresholding

- Original image is displayed.
- Adaptive Mean Thresholded image is displayed.
- Adaptive Gaussian Thresholded image is displayed.
- Threshold values vary across different regions of the image.
- Suitable for images with uneven illumination.

### Otsu's Thresholding

- Original image is displayed.
- Otsu segmented image is displayed.
- Optimal threshold value is calculated automatically.
- Produces improved segmentation for bimodal histograms.

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Load the input image using OpenCV.

### Step 3:

Convert the input image into grayscale format.

### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.

### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program

## Developed By

**Name:** Rishikesh S

**Register No:** 212225240118


### Original Image
```
import cv2
import matplotlib.pyplot as plt
import numpy as np

image = cv2.imread('Tower.jpg')
image = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image)  # Convert from BGR to RGB for display
plt.title("Original Image")
plt.axis('off')
```

<img width="1680" height="1224" alt="image" src="https://github.com/user-attachments/assets/43105c6e-4c8e-4d66-9d4b-6d1f6814c260" />


### ORIGINAL grayscale image

```
gray_image = cv2.cvtColor(image, cv2.COLOR_RGB2GRAY)  # Convert to grayscale
plt.imshow(gray_image,cmap = 'gray')  
plt.title("Grayscale Image")
plt.axis('off')
```

<img width="1686" height="1224" alt="image" src="https://github.com/user-attachments/assets/79763e58-0719-4559-aa74-b4648773051d" />


### Global Thresholding

```
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()
```

<img width="1671" height="1221" alt="image" src="https://github.com/user-attachments/assets/d90a0b02-3302-4f31-a6e7-f7f11b8e0258" />



### Adaptive Thresholding

```
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
plt.imshow(result, cmap="gray")
plt.title("Adaptive Thresholding")
plt.axis("off")
plt.show()
```

<img width="1665" height="1221" alt="image" src="https://github.com/user-attachments/assets/2112f2ba-17dc-4cbc-9378-fab69cc8bbc0" />


### Otsu's Thresholding

```
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()
```

<img width="1671" height="1212" alt="image" src="https://github.com/user-attachments/assets/713f72bf-b4ab-4590-835c-1988442ad2b6" />



## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
