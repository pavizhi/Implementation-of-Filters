# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import All The Necessary Modules.
### Step 2:
Using Averaging Filter Smoothen the given image.
### Step 3:
Using the Weighted Averaging Filter Smoothen the given Image.
### Step 4:
Using the Gaussian Filter Smoothen the given Image.
### Step 5:
Using the Median Filter Smoothen the given Image.
### Step 6:
Using the Laplacian Kernel Filter Sharpen the given Image.
### Step 7:
Using the Laplacian Operator Filter Sharpen the given Image.


## Program:
### Developed By   : B.PAVIHI
### Register Number: 212221230077
</br>

### 1. Smoothing Filters
i) Using Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('1.png')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernel = np.ones ((11,11), np.float32)/121
image3=cv2.filter2D(image2,-1, kernel)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```
ii) Using Weighted Averaging Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('1.png')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernal2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16 
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```
iii) Using Gaussian Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('1.png')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
gaussian_blur=cv2.GaussianBlur(src=image2,ksize=(11,11),sigmaX=0,sigmaY=0)
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```
iv) Using Median Filter
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('1.png')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
median=cv2.medianBlur(src=image2, ksize=11)
image3 = cv2.filter2D(image2,-1,kernal2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```

### 2. Sharpening Filters
i) Using Laplacian Kernel
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('1.png')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
kernel3=np.array([[0,1,0],[1,-4,1],[0,1,0]])
image3=cv2.filter2D(image2,-1, kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```
ii) Using Laplacian Operator
```Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread('1.png')
image2=cv2.cvtColor (image1,cv2.COLOR_BGR2RGB) 
new_image = cv2.Laplacian(image2, cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1) 
plt.imshow(image2)
plt.title('Orignal') 
plt.axis('off')
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
![image](https://user-images.githubusercontent.com/95067176/231179242-aab507aa-691b-4d23-a6f7-ee003abcf825.png)
</br>

ii) Using Weighted Averaging Filter
</br>
![image](https://user-images.githubusercontent.com/95067176/231179711-9191b513-c4a9-40ad-9d65-c53477dc2cd9.png)
</br>

iii) Using Weighted Averaging Filter
</br>
![image](https://user-images.githubusercontent.com/95067176/231180143-eb15a9e4-a2cf-4252-a211-08c10e905f6a.png)
</br>

iv) Using Median Filter
</br>
![image](https://user-images.githubusercontent.com/95067176/231185921-c49d96cc-b24b-4cd9-9e12-587385893adc.png)
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernel
</br>
![image](https://user-images.githubusercontent.com/95067176/231186837-df524e6d-91e7-4abf-9178-de8d3357b11d.png)
</br>

ii) Using Laplacian Operator
</br>
![image](https://user-images.githubusercontent.com/95067176/231187002-957f6e0f-5245-4c12-8fd6-6839c5800ebc.png)
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
