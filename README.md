# Implementation of Erosion and Dilation Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program
```

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 1: Load the selected image
image_path = r"C:\Users\acer\OneDrive\Pictures\Camera Roll\virat_kohli.jpg"
img = cv2.imread(image_path)

# Step 2: Convert to grayscale
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)

# Step 3: Create structuring element
kernel = np.ones((5, 5), np.uint8)

# Step 4: Apply erosion
erosion = cv2.erode(gray, kernel, iterations=1)

# Step 5: Apply dilation
dilation = cv2.dilate(gray, kernel, iterations=1)

# Step 6: Display all images
plt.figure(figsize=(12, 8))

plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")

plt.subplot(2, 2, 2)
plt.imshow(gray, cmap="gray")
plt.title("Grayscale Image")
plt.axis("off")

plt.subplot(2, 2, 3)
plt.imshow(erosion, cmap="gray")
plt.title("Eroded Image")
plt.axis("off")

plt.subplot(2, 2, 4)
plt.imshow(dilation, cmap="gray")
plt.title("Dilated Image")
plt.axis("off")

plt.tight_layout()
plt.show()

print("Image Erosion and Dilation completed successfully!")

```

## Developed By

**Name: PON SARAVANA PANDIAN B**

**Register No: 212225230207**

## Output

<img width="1372" height="435" alt="image" src="https://github.com/user-attachments/assets/bf8bd753-f7ca-4489-b4df-89ca0d740d11" />

<img width="1377" height="483" alt="image" src="https://github.com/user-attachments/assets/b1d7500b-78e7-4713-93ed-19dfe9dbc3b9" />


### Original Image

- A text image containing characters is displayed.
- The image serves as the input for morphological processing.

### Erosion

- Original image is displayed.
- Eroded image is displayed.
- The thickness of the characters is reduced.
- Object boundaries shrink inward.

### Dilation

- Original image is displayed.
- Dilated image is displayed.
- The thickness of the characters increases.
- Object boundaries expand outward.

## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
