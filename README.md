# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
  Import the necessary libraries: OpenCV (cv2), NumPy (np), and Matplotlib (plt).


### Step2:
  Use cv2.putText to add the text "THE BOYS" to the image at coordinates (10, 70) with a font size of 2 and white color (255).

### Step3:
  Use cv2.getStructuringElement to create a kernel (structuring element) for morphological operations. In this case, it's a rectangular kernel of size (9, 9).


### Step4:
  Use cv2.morphologyEx with the cv2.MORPH_CLOSE operation to perform a closing operation on the original image.

### Step5:

  Use plt.show() to display the entire figure with the subplots
 
## Program:


# Import the necessary packages
``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

# Create the Text using cv2.putText
``` Python
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'THE BOYS',(10,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()
```

# Create the structuring element
``` Python
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))


```
# Use Opening operation

``` Python
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()
```


# Use Closing Operation
``` Python
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()
```



## Output:

### Display the input Image
<br>
<br>
<br>



![image](https://github.com/praveenst13/OPENING--CLOSING/assets/118787793/8a93606c-da80-4c18-912a-7aeffe25a2dc)

<br>
<br>
<br>

### Display the result of Opening
<br>
<br>
<br>

![image](https://github.com/praveenst13/OPENING--CLOSING/assets/118787793/cf717145-571e-4db8-b996-c6e6ba2d6262)



<br>
<br>
<br>

### Display the result of Closing
<br>
<br>
<br>

![image](https://github.com/praveenst13/OPENING--CLOSING/assets/118787793/bf3b7e0f-8ce8-4d42-b311-25aa04cbab4f)


<br>
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
