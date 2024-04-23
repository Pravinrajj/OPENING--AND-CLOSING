# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.
 
## Program:
```
DEVELOPED BY: PRAVINRAJJ G.K
REGISTER NO: 212222240080
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'NIKA', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (10,7))

# Use Opening operation
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

# Use Closing Operation
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")
```
## Output:

### Display the input Image
![image](https://github.com/Pravinrajj/OPENING--AND-CLOSING/assets/117917674/b82557c3-ba85-49bd-a2b6-b0a147e61354)

### Display the result of Opening
![image](https://github.com/Pravinrajj/OPENING--AND-CLOSING/assets/117917674/fff006fe-8359-49ee-867a-86986a5d0ac4)

### Display the result of Closing
![image](https://github.com/Pravinrajj/OPENING--AND-CLOSING/assets/117917674/aef47012-2d72-43cf-8de8-248bb136d67b)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
