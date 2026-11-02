# CANNY-EDGE-DETECTION-OPENCV

## Aim

To perform edge detection on an input image using the Canny Edge Detection technique in OpenCV to identify and highlight significant edges based on intensity gradients and thresholding.

---

## Software Required

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (`cv2`)
- NumPy
- Matplotlib

---

## ⚙️ Algorithm

### Step 1:
Import the necessary Python libraries, including OpenCV (`cv2`), NumPy, and Matplotlib.

### Step 2:
Load the input image using `cv2.imread()`.

### Step 3:
Convert the loaded color image into a grayscale image using `cv2.cvtColor()`.

### Step 4:
Apply Gaussian Blur to the grayscale image using `cv2.GaussianBlur()` to reduce noise and unwanted details.

### Step 5:
Apply the Canny Edge Detection algorithm using `cv2.Canny()` with suitable lower and upper threshold values (50 and 150).

### Step 6:
Calculate the intensity gradients to identify potential edges in the image.

### Step 7:
Perform non-maximum suppression to thin the detected edges and apply double thresholding to classify strong, weak, and non-edge pixels.

### Step 8:
Apply edge tracking by hysteresis to connect weak edges associated with strong edges and eliminate unwanted edges.

### Step 9:
Display the original image and the resulting Canny edge-detected image using Matplotlib.

---

## Developed By

- **Name:** SHRIVARSHAN P G
- **Register No:** 212225240146

---

## Program

```python
import cv2
import matplotlib.pyplot as plt

img = cv2.imread('sv.jpeg',cv2.IMREAD_GRAYSCALE)

blurred =cv2.GaussianBlur(img, (5,5),0)

edges = cv2.Canny(blurred, 50, 150) 

plt.figure(figsize=(10,5))
plt.subplot(121),plt.imshow(img, cmap='gray')
plt.title('Original Image'), plt.axis('off')
plt.subplot(122),plt.imshow(edges, cmap='gray')
plt.title('Detected Edges'), plt.axis('off')
plt.show()
```
## Ouput

### Original Image and Detected Edges

<img width="1045" height="320" alt="image" src="https://github.com/user-attachments/assets/c649b670-5f74-4117-8418-7bc01fba1cda" />


---

## Result

Thus, edge detection was successfully performed on the input image using the Canny Edge Detection technique in OpenCV. The algorithm identified and highlighted significant edges by applying Gaussian smoothing, gradient calculation, non-maximum suppression, double thresholding, and edge tracking by hysteresis.
