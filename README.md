# Image-Acquisition-from-Web-Cameraa
## Aim
 
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:

Use VideoCapture(0) to access web camera
### Step 2:

Use imread to read the video or image

### Step 3:

Use imwrite to save the image

### Step 4:

Use imshow to show the video


### Step 5:
End the program and close the output video windows by pressing 'q'.
##  Program:
```

Developed By:SHARMILA A
Register No:212221230094
```


## i) Write the frame as JPG file
```
import cv2
videoCaptureObject = cv2.VideoCapture(0)
while (True):
    ret,frame = videoCaptureObject.read()
    cv2.imwrite("D1.jpeg",frame)
    result = False
videoCaptureObject.release()
cv2.destroyAllWindows()

```

## ii) Display the video
```
import cv2
videoCaptureObject = cv2.VideoCapture(0)
while(True):
    ret,frame = videoCaptureObject.read()
    cv2.imshow('212221230094 SHARMILA ',frame)
    if cv2.waitKey(1) == ord('q'):
        break
videoCaptureObject.release()
cv2.destroyAllWindows()
```


## iii) Display the video by resizing the window
```
import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read() 
    width = int(cap.get(3))
    height = int(cap.get(4))
    image = np.zeros(frame.shape, np.uint8) 
    smaller_frame = cv2.resize(frame, (0,0), fx = 0.5, fy=0.5) 
    image[:height//2, :width//2] = smaller_frame
    image[height//2:, :width//2] = smaller_frame
    image[:height//2, width//2:] = smaller_frame 
    image [height//2:, width//2:] = smaller_frame
    cv2.imshow('212221230094 SHARMILA', image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()

```
## iv) Rotate and display the video
```
import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
    ret, frame = cap.read() 
    width = int(cap.get(3))
    height = int(cap.get(4))
    image = np.zeros(frame.shape, np.uint8) 
    smaller_frame = cv2.resize(frame, (0,0), fx = 0.5, fy=0.5) 
    image[:height//2, :width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[:height//2, width//2:] = smaller_frame 
    image [height//2:, width//2:] = smaller_frame
    cv2.imshow('myimage', image)
    if cv2.waitKey(1) == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()








```

## Output

### i) Write the frame as JPG image
![v1](https://github.com/Sharmilasha/Image-Acquisition-from-Web-Cameraa/assets/94506182/9bf63f1c-38f4-4d64-a9b0-84e316139ef1)


### ii) Display the video
![v1](https://github.com/Sharmilasha/Image-Acquisition-from-Web-Cameraa/assets/94506182/99b6041c-cdd8-45bc-873f-7a9db66e2d5b)



### iii) Display the video by resizing the window
![v2](https://github.com/Sharmilasha/Image-Acquisition-from-Web-Cameraa/assets/94506182/79050434-8700-4a97-87e6-99351e6d9b39)




### iv) Rotate and display the video

![v3](https://github.com/Sharmilasha/Image-Acquisition-from-Web-Cameraa/assets/94506182/1c1b2ca8-e5a5-4d58-b312-d122c1b5df7d)




## Result:
Thus the image is accessed from webcamera and displayed using openCV.
