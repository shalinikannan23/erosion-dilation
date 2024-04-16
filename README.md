# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

- Step1: Import the necessary packages.
- Step2: Use cv2.putText to add the text to the image at specific coordinates.
- Step3: Define two kernels (kernel and kernel1) for morphological operations.
- Step4: Display the eroded image using cv2.imshow.
- Step5: Display the dilated image using cv2.imshow.

 ```
DEVELOPED BY: SHALINI K
REGISTER NUMBER: 212222240095
```

## Program:

- Import the necessary packages
  
  ```PY
  import cv2
  import numpy as np
  ```

- Create the Text using cv2.putText

  ```py
  img1=np.zeros((100,500),dtype="uint8")
  font=cv2.FONT_HERSHEY_PLAIN
  cv2.putText(img1,"SHALINI K 212222240095",(5,60),font,2,(255),5,cv2.LINE_AA)
  cv2.imshow("Original Image",img1)
  cv2.waitKey(0)
  ```
  ![image](https://github.com/shalinikannan23/erosion-dilation/assets/118656529/618cfdc2-afef-4532-b4d6-285c8eb90abf)
  
- Create the structuring element

```PY
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```

- Erode the image

  ```PY
  cv2.erode(img1, kernel)
  image_erode = cv2.erode(img1,kernel1)
  cv2.imshow("Erode Image",image_erode)
  cv2.waitKey(0)
  ```
  ![image](https://github.com/shalinikannan23/erosion-dilation/assets/118656529/60f262f0-4d9a-4844-a8c5-04e97ad4db3a)

- Dilate the image

  ```PY
  image_dilatel=cv2.dilate(img1,kernel1)
  cv2.imshow("Dilate Image",image_dilatel)
  cv2.waitKey(0)
  ```
  ![image](https://github.com/shalinikannan23/erosion-dilation/assets/118656529/2079c4e8-faaf-4d28-aaa4-b93940d681ec)


## Result:
Thus the generated text image is eroded and dilated using python and OpenCV.
