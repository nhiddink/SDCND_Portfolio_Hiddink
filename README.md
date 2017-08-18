<<<<<<< HEAD
<<<<<<< HEAD
<<<<<<< HEAD
<<<<<<< HEAD
<<<<<<< HEAD
# SDCND_Portfolio_Hiddink
=======
#**Finding Lane Lines on the Road** 
<img src="laneLines_thirdPass.jpg" width="480" alt="Combined Image" />

When we drive, we use our eyes to decide where to go.  The lines on the road that show us where the lanes are act as our constant reference for where to steer the vehicle.  Naturally, one of the first things we would like to do in developing a self-driving car is to automatically detect lane lines using an algorithm.

In this project you will detect lane lines in images using Python and OpenCV.  OpenCV means "Open-Source Computer Vision", which is a package that has many useful tools for analyzing images.  

**Step 1:** Getting setup with Python

To do this project, you will need Python 3 along with the numpy, matplotlib, and OpenCV libraries, as well as Jupyter Notebook installed. 

We recommend downloading and installing the Anaconda Python 3 distribution from Continuum Analytics because it comes prepackaged with many of the Python dependencies you will need for this and future projects, makes it easy to install OpenCV, and includes Jupyter Notebook.  Beyond that, it is one of the most common Python distributions used in data analytics and machine learning, so a great choice if you're getting started in the field.

Choose the appropriate Python 3 Anaconda install package for your operating system <A HREF="https://www.continuum.io/downloads" target="_blank">here</A>.   Download and install the package.

If you already have Anaconda for Python 2 installed, you can create a separate environment for Python 3 and all the appropriate dependencies with the following command:

`>  conda create --name=yourNewEnvironment python=3 anaconda`

`>  source activate yourNewEnvironment`

**Step 2:** Installing OpenCV

Once you have Anaconda installed, first double check you are in your Python 3 environment:

`>python`    
`Python 3.5.2 |Anaconda 4.1.1 (x86_64)| (default, Jul  2 2016, 17:52:12)`  
`[GCC 4.2.1 Compatible Apple LLVM 4.2 (clang-425.0.28)] on darwin`  
`Type "help", "copyright", "credits" or "license" for more information.`  
`>>>`   
(Ctrl-d to exit Python)

run the following command at the terminal prompt to get OpenCV:

`>  conda install -c https://conda.anaconda.org/menpo opencv3`

then to test if OpenCV is installed correctly:

`> python`  
`>>> import cv2`  
`>>>`  
(Ctrl-d to exit Python)

**Step 3:** Installing moviepy  

We recommend the "moviepy" package for processing video in this project (though you're welcome to use other packages if you prefer).  

To install moviepy run:

`>pip install moviepy`  

and check that the install worked:

`>python`  
`>>>import moviepy`  
`>>>`  
(Ctrl-d to exit Python)

**Step 4:** Opening the code in a Jupyter Notebook

You will complete this project in a Jupyter notebook.  If you are unfamiliar with Jupyter Notebooks, check out <A HREF="https://jupyter-notebook-beginner-guide.readthedocs.io/en/latest/" target="_blank">this link</A> to get started.

Jupyter is an ipython notebook where you can run blocks of code and see results interactively.  All the code for this project is contained in a Jupyter notebook. To start Jupyter in your browser, run the following command at the terminal prompt (be sure you're in your Python 3 environment!):

`> jupyter notebook`

A browser window will appear showing the contents of the current directory.  Click on the file called "P1.ipynb".  Another browser window will appear displaying the notebook.  Follow the instructions in the notebook to complete the project.  
>>>>>>> CarND_P1_Finding_Lane_Lines/master
=======
# Self-Driving Car Engineer Nanodegree
# Deep Learning
## Project: Build a Traffic Sign Recognition Program

### Overview

In this project, you will use what you've learned about deep neural networks and convolutional neural networks to classify traffic signs. You will train a model so it can decode traffic signs from natural images by using the [German Traffic Sign Dataset](http://benchmark.ini.rub.de/?section=gtsrb&subsection=dataset). After the model is trained, you will then test your model program on new images of traffic signs you find on the web, or, if you're feeling adventurous pictures of traffic signs you find locally!

### Dependencies

This project requires **Python 3.5** and the following Python libraries installed:

- [Jupyter](http://jupyter.org/)
- [NumPy](http://www.numpy.org/)
- [SciPy](https://www.scipy.org/)
- [scikit-learn](http://scikit-learn.org/)
- [TensorFlow](http://tensorflow.org)

Run this command at the terminal prompt to install [OpenCV](http://opencv.org/). Useful for image processing:

- `conda install -c https://conda.anaconda.org/menpo opencv3`

### Dataset

1. Download the dataset. You can download the pickled dataset in which we've already resized the images to 32x32 [here](https://d17h27t6h515a5.cloudfront.net/topher/2016/October/580d53ce_traffic-sign-data/traffic-sign-data.zip).
 
2. Clone the project and start the notebook.
```
git clone https://github.com/udacity/traffic-signs
cd traffic-signs
jupyter notebook Traffic_Signs_Recognition.ipynb
```
3. Follow the instructions in the `Traffic_Signs_Recognition.ipynb` notebook.

>>>>>>> CarND_P2_Traffic_Sign_Classifier/master
=======
![ScreenShot](images/loading_screen.png)
# Udacity's Self-Driving Car Nanodegree Program
## Project 3 - Behavioral Cloning
### _How to Train a Deep Neural Network to Drive a Simulated Car_ 
This project builds and implements a behavioral cloning (end-to-end) network that drives a simulated autonomous vehicle around two different test tracks. The first track is used to generate data that the car will use to react and recover in changing road conditions. The second track is used to test the model's performance and ensure that it is not overfitting the data after training.

![ScreenShot](images/main_menu.png)
**"TRAINING MODE"** is used to collect data on the simulator for several laps and automatically saves data to **driving_log.csv**.
**"AUTONOMOUS MODE"** Driving simulation is accomplished by running the car's drive server using the following code from the Terminal after a cd into the project's directory:

#### $ python drive.py model.json

The first track, shown below, is used to record data and validate the model after training.
![ScreenShot](images/first_track.png)

The following naming conventions have been used in this project:

+ **model.py** - The script used to create and train the model. SDCND_P3_Hiddink.ipynb serves as the de facto model.py script in this implementation. This allowed the use of Jupyter notebooks and made up-front code writing more straightforward.

+ **drive.py** - The script to drive the car. The original file was kept largely the same, with the exception of a crop function. The script is in the home directory as drive.py.

+ **model.json** - The model architecture. The **archive** folder contains the historical versions of the model, model.json, that were created throughout this project's development.

+ **model.h5** - The model weights. The **archive** folder contains the historical versions of the model's weights, model.h5, that were created throughout this project's development.

+ **README.md** - explains the structure of your network and training approach. This is the **README.md** file.

### Model Architecture

![ScreenShot](images/model_architecture.png)

The graph above shows the NVIDIA model architecture described in a recent paper published here: https://arxiv.org/pdf/1604.07316v1.pdf 

This project was largely inspired by the NVIDIA architecture, in addition to other successful implementations of Convolutional Neural Networks on GitHub, such as comma.ai (https://github.com/commaai/research) and student repos by ksakmann (https://github.com/ksakmann/CarND-BehavioralCloning/) and diyjac (https://github.com/diyjac/SDC-P3). 

Although slightly different in their approaches, each of the models mentioned above have the same thing in common: the data that they were supplied was heavily augmented in several ways in order to increase the model's exposure to changing road conditions. This project draws heavily on these techniques, and attempts to combine them for increased performance.

The model is built using the Keras library and is a Convolutional Neural Network (CNN) with four convolutional layers. The sizes of each layer were chosen to decrease the kernel size by a factor of 2 after each convolution. ReLu activations are used throughout the model, and two dropout layers help to reduce the tendancy toward overfitting.

### Training the Model (model.py)

Below is the second track available in the simulator. Once the model is trained, this track used to verify performance on new terrain.
![ScreenShot](images/second_track.png)
The model was trained in the SDCND_P3_Hiddink.ipynb jupyter notebook using the model described above. Unfortunately, data input was limited due to several factors, including, but not limited to, the following:
+ The data collected via keyboard input was too "choppy", i.e. it did not acutely record the correct maneuvers the model should make to recover from the edges of the road.
+ A joystick was not available to collect driving data.

As a result, it became necessary to augment the data set provided by Udacity using several techniques, as shown below.
Original Sample:

![ScreenShot](images/sample_feature.jpg)

+ Shearing
![ScreenShot](images/random_shear.jpg)

+ Cropping
![ScreenShot](images/random_crop.jpg)

+ Flipping
![ScreenShot](images/random_flip.jpg)

+ Adjusting Brightness 
![ScreenShot](images/random_brightness.jpg)

Each of these techniques were used to increase the overall size of the data set to give the model more material to learn.

#### Final Results
Here are the final results of the project:

[![Alt text](https://img.youtube.com/vi/kuUtfNDPWpY/0.jpg)](https://www.youtube.com/watch?v=kuUtfNDPWpY)

#### Further plans
In the future, I hope to improve upon the data augmentation techniques to increase performance in shadows. Additionally, I could to add additional tracks to the simulator and possibly implement lane detection using OpenCV. 

One project on GitHub that has inspired me further is TensorKart by Kevin Hughes (https://github.com/kevinhughes27/TensorKart). I am interested in contributing further to his work, possibly using some of the code that was developed in this project.

[![Alt text](https://img.youtube.com/vi/vrccd3yeXnc/0.jpg)](https://www.youtube.com/watch?v=vrccd3yeXnc)
>>>>>>> CarND_P3_Behavioral_Cloning/master
=======
[//]: # (Image References)
[loading_screen]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/Resources/Screenshots/loading_screen.png
[distortion]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/resources/output_images/distortion.png
[distortion_theory]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/Resources/Screenshots/distortion.png
[corners_unwarp]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/resources/output_images/corners_unwarp.png
[distortion_corrected]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/resources/output_images/undistorted.png
[sobel_x]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/resources/output_images/sobel_x.png
[sobel_y]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/resources/output_images/sobel_y.png
[gradient_magnitude]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/resources/output_images/gradient_magnitude.png
[gradient_direction]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/resources/output_images/gradient_direction.png 
[color_thresholds]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/resources/output_images/color_thresholds.png 
[multiple_thresholds]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/resources/output_images/thresholded_binary.png
[region_masked]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/resources/output_images/region_masked.png
[perspective_transform]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/resources/output_images/perspective_transform.png
[sliding_windows]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/resources/output_images/sliding_windows.png
[shaded_lanes]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/resources/output_images/shaded_lanes.png
[lane_mapping]: https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding/blob/master/resources/output_images/lane_mapping.png

![alt text][loading_screen]
## Udacity's Self-Driving Car Nanodegree Program
### Project 4 - Advanced Lane Finding

---

This project utilizes several computer vision algorithms and techniques to perform advanced lane finding on test images and video streams. There are several steps involved in this process, including: 

* Computing the camera calibration matrix and distortion coefficients given a set of chessboard images.
* Applying a distortion correction to raw images.
* Using color transforms, gradients, etc., to create a thresholded binary image.
* Appling a perspective transform to rectify binary image ("birds-eye view").
* Detecting lane pixels and fit to find the lane boundary.
* Determining the curvature of the lane and vehicle position with respect to center.
* Warping the detected lane boundaries back onto the original image.
* Outputing the visual display of the lane boundaries and numerical estimation of lane curvature and vehicle position.

###Camera Calibration

The code for this step is contained in Sections I & II of SDCND_P4_Hiddink.ipynb.  

![alt text][distortion]

First, I define "object points", which represent the (x, y, z) coordinates of the chessboard corners in the world. I assume that the chessboard is fixed on the (x, y) plane at z=0, such that the object points are the same for each calibration image.  Thus, `objp` is just a replicated array of coordinates, and `objpoints` is appended with a copy of it every time I successfully detect all chessboard corners in a test image.  `imgpoints` is appended with the (x, y) pixel position of each of the corners in the image plane with each successful chessboard detection.  

![alt text][distortion_theory]

From there, I used the output `objpoints` and `imgpoints` to compute the camera calibration and distortion coefficients using the `cv2.calibrateCamera()` function.  I applied this distortion correction to the test image using the `cv2.undistort()` function and obtained this result: 

![alt text][corners_unwarp]

Here are the results of distortion correction on each of the test images (located in the test_images folder):

![alt text][distortion_corrected]

---

###Pipeline (Images)

![alt text][multiple_thresholds]

The example above displays the results of multiple thresholds on each test image in the test_images folder. Section III of the code explains this process step-by-step, with examples of each individual threshold. In order, the thresholding used on the images is as follows:

+ Color Channel HLS & HSV Thresholding - I extract the S-channel of the original image in HLS format and combine the result with the extracted V-channel of the original image in HSV format.

![alt text][color_thresholds]

+ Binary X & Y - I use Sobel operators to filter the original image for the strongest gradients in both the x-direction and the y-direction.

![alt text][sobel_x]
![alt text][sobel_y]

Next, I used techniques from "Project 1 - Finding Lane Lines" to conduct sanity checks. These techniques included Region Masking & Hough Lines, and the purpose for performing them was to ensure that the thresholding steps I took were accurate enough to yield proper perspective transforms.

The region masking results are shown below. I chose to limit the mask to a region with the following points: 

| Point       | Value                                    | 
|:-----------:|:----------------------------------------:| 
| Upper Left  | (image width x 0.4, image height x 0.65) | 
| Upper Right | (image width x 0.6, image height x 0.65) |
| Lower Right | (image width, image height)              |
| Lower Left  | (0, image height)                        |

![alt text][region_masked]

The code for my perspective transform is performed in a function I created called perspective_transform. The function takes in a thresholded binary image and source points, with the source points coinciding with the region masking points explained in the region masking table above. For destination points, I chose the outline of the image being transformed. Here are the results of the transforms:

![alt text][perspective_transform]

The next step after transforming the perspective was to detect lane-line pixels and to fit their positions using a polynomial in Section V of my code. After developing functions for sliding_windows and shaded_lanes, I was able to detect the lanes and yield the following results:

Sliding Windows Technique:
![alt text][sliding_windows]

Shaded Lanes Technique:
![alt text][shaded_lanes]

After detecting the lanes I needed to calculate the radius of curvature for each of the polynomial fits that I performed. The results of these calculations are shown in the table below. I used the radius of curvature example code from Udacity's lessons to create the calculation cells.

| Test Image | Radius of Curvature (Left) | Radius of Curvature (Right) | 
|:----------:|:--------------------------:|:---------------------------:| 
| test1.png  | 2985.467894 meters         | 2850.142018 meters          | 
| test2.png  | 4984.505982 meters         | 12357.329365 meters         |
| test3.png  | 10088.084712 meters        | 2363.421967 meters          |
| test4.png  | 9894.520013 meters         | 2366.846436 meters          |
| test5.png  | 2548.327638 meters         | 6124.849321 meters          |
| test6.png  | 4173.313472 meters         | 45794.832663 meters         |

Another calculation performed was the offset from the lane's center. The calculations are shown in the code cell following the radius of curvature, and yielded the following:

| Test Image | Offset from Center |
|:----------:|:------------------:| 
| test1.png  | 1.020143 meters    |
| test2.png  | 0.901214 meters    |
| test3.png  | 0.935571 meters    |
| test4.png  | 1.123214 meters    |
| test5.png  | 0.930286 meters    |
| test6.png  | 1.070357 meters    |

Finally, I plotted the warped images back down onto the road such that, for each image, the lane area is identified clearly:

![alt text][lane_mapping]

---

### Pipeline (Video)

Click on the image or link below to view the video results of the project.

### P4_video_final.mp4
https://youtu.be/5ZKbpNY-rok

<a href="http://www.youtube.com/watch?feature=player_embedded&v=5ZKbpNY-rok
" target="_blank"><img src="http://img.youtube.com/vi/5ZKbpNY-rok/0.jpg" 
alt="YouTube" width="240" height="180" border="10" /></a>

### 

=======
[//]: # (Image References)
[color_classification]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/output_images/color_classification.png
[color_distribution_visualization]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/output_images/color_distribution_visualization.png
[color_histograms_visualization]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/output_images/color_histograms_visualization.png
[data_visualization]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/output_images/data_visualization.png
[distortion]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/screenshots/distortion.png
[gradient_visualization]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/output_images/gradient_visualization.png
[heatmap]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/output_images/heatmap.png
[hog_classification]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/output_images/hog_classification.png
[hog_visualization]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/output_images/hog_visualization.png
[loading_screen]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/screenshots/loading_screen.png
[one_box_per_car]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/output_images/one_box_per_car.png
[random_image_visualization]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/output_images/random_image_visualization.png
[sliding_windows]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/output_images/sliding_windows.png
[spatial_binning_visualization]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/output_images/spatial_binning_visualization.png
[undistorted]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/output_images/undistorted.png
[undistorted_and_warped]: https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/output_images/undistorted_and_warped.png

[![loading_screen](https://github.com/nhiddink/CarND_P5_Vehicle_Detection_and_Tracking/blob/master/resources/screenshots/loading_screen.png)](http://www.udacity.com/drive)
## Udacity's Self-Driving Car Nanodegree Program
### Project 5 - Vehicle Detection and Tracking

---

The software pipeline in SDCND_P5_Hiddink.ipynb is written to detect vehicles in a video stream. To accomplish this, the following steps were performed:
+ **Camera Calibration** - correct distortion due to the camera lens that was used to record the test videos. 
+ **Data Visualization** - understand the labeled data set as two labeled groups, "cars" and "not-cars".
+ **Feature Extraction** - apply five techniques, including histograms of color, color distribution, spatial binning, gradient magnitude, and Histogram of Oriented Gradients (HOG), on the labeled training set of images to create a feature vector.
+ **Preprocessing Data** - normalize, randomize, and split the labeled data into a training set, a validation set, and a testing set.
+ **Training** -  train a Linear SVM classifier on the labeled training set
+ **Sliding Windows** - implement a technique to search an image for vehicles using the trained classifier, and optimize the algorithm's efficiency by limiting the search area of the image and/or using heat maps that reject outliers of the positive windows.
+ **Video** - run a function using moviepy that estimates a bounding box for detected vehicles frame by frame.

Each of these steps is described in detail below.

---

### Camera Calibration

The code for this step is contained in Section I of SDCND_P5_Hiddink.ipynb.

![undistorted]

In order to account for distortion, the camera used to record the project video and shoot the test images needs to be calibrated. To do this, a series of chessboard images were introduced that displayed varying distortion angles. 

![distortion]

First, I define "object points", which represent the (x, y, z) coordinates of the chessboard corners in the world. I assume that the chessboard is fixed on the (x, y) plane at z=0, such that the object points are the same for each calibration image. Thus, objp is just a replicated array of coordinates, and objpoints is appended with a copy of it every time I successfully detect all chessboard corners in a test image. imgpoints is appended with the (x, y) pixel position of each of the corners in the image plane with each successful chessboard detection.

![undistorted_and_warped]

From there, I used the output objpoints and imgpoints to compute the camera calibration and distortion coefficients using the cv2.calibrateCamera() function. I applied this distortion correction to the test image using the cv2.undistort() function and obtained the result shown above. After successfully warping chessboard images, I was able to apply the undistort function to the test images and videos using a pickle file that stored the distortion matrix.

---

### Data Visualization

The following is a visualization of the first 10 images in the labeled dataset:

![data_visualization]

Each image is defined with either a "car" or "not-car" label. The labeled data sets used in this project are originally from the GTI Vehicle Image Database [GTI Vehicle Image Database](http://www.gti.ssr.upm.es/data/Vehicle_database.html), augmented by examples extracted from the project video itself. In the future, this repository will include images from the [KITTI Vision Benchmark Suite](http://www.cvlibs.net/datasets/kitti/) and the ecently released [Udacity Labeled Dataset](https://github.com/udacity/self-driving-car/tree/master/annotations), as described in the Future Plans section below.

---

### Feature Extraction

Several different techniques for feature extraction were used in Section 2 of  this project, including histograms of color, color distribution, spatial binning, gradient magnitude, and Histogram of Oriented Gradients (HOG). Each has its own effect on the feature vector that is produced, and when combined the techniques tend to improve the chosen classifier's performance.

**Histograms of Color**

Histograms of color are used to analyze the raw pixel intensities of each color channel as features in the image. Given an image in RGB color space, color histograms of features return a concatenated feature vector based on the number of intensity bins and pixel intensity ranges.

![color_histograms_visualization]


**Color Distribution**

Color distribution maps are useful in studying color values and locating clusters of color that correspond to objects of interest in an image. When plotting these maps in 3D, often the color distribution of objects of interest is conveniently clustered along a plane.

![color_distribution_visualization]

**Spatial Binning**

Raw pixel values are useful to include in the feature vector when the desired objects in an image remain identifiable at low image resolutions, such as a car object.

![spatial_binning_visualization]

**Gradient Magnitude**

Gradient magnitude is a technique used in previous computer vision projects (Projects 1 & 4) that applies a filter that represents the magnitude of the sobel-x and sobel-y gradients of odd-numbered pixel squares, such as 3x3 or 5x5.

![gradient_visualization]

**Histogram of Oriented Gradients (HOG)**

HOG feature extraction is the most important technique utilized in this project. The scikit-image package has a built in function to handle HOG extraction, which is tuned by parameters including orientations, pixels_per_cell, and cells_per_block.

![hog_visualization]

The final feature extraction method that was implemented includes color histograms, spatial binning, and HOG, as shown in Sections 2 & 3. For HOG, the parameters were chosen as follows:

| Parameter       | Value   |
|:---------------:|:-------:| 
| orientations    | 9       |                                                                                 
| pixels_per_cell | (16,16) |
| cells_per_block | (4,4)   |
| visualise       | True    |
| feature_vector  | False   |

I chose these parameters for HOG after trial and error on test4.jpg. As shown in the visualization above, the parameters optimize the gradients, and work well for the heat map step later in the pipeline that limits the false positive classifications.

---

### Preprocessing Data

The training data was normalized, randomized, and split into training and testing sets, with 20% of the data reserved for the testing set.

---

### Training the SVC Classifier

After exploring feature extraction techniques, I trained a SVC classifier to classify the dataset as "car" or "not-car". On a consistent basis, the accuracy for this classifier was above 94%. To do this, I analyzed two different feature vectors and ran them through the classfier to produce the following results:

**Classification by Color and Spatial Binning**
![color_classification]

**Classification by HOG**
![hog_classification]

After comparing these two results, I decided to encorporate both of them as one feature vector that I retrained prior to running sliding windows on the test image, as explained next.

---

### Sliding Windows Search

![sliding_windows]

Section 3 of SDCND_P5_Hiddink.ipynb outlines my sliding windows approach to searching for vehicles in a test image with my SVC classifier. I decided to leave the scale at 1, but found that it performed well. I limited the search area to the bottom half of the image, minus the bottom 10%, for a total of 40% of the image to lower the total number of windows I needed to make. The parameters I chose for the sliding windows themselves are as follows: 

| Parameter  | Value             |
|:----------:|:-----------------:| 
| y_start    | image width x 0.5 |  
| y_stop     | image width x 0.9 |
| xy_window  | (64,64)           |
| xy_overlap | (0.85, 0.85)      |

These parameters produced the following results:

![positive_window_detections]

The overlap of 0.85 allowed for a strong signature of positive window values on the actual cars that simplified the process of ruling out false positives with heat maps, as shown in the image below:

![heatmap]

After recording the positions of positive detections in each frame of the video, I created a heatmap and thresholded it to identify vehicle positions. I then used `scipy.ndimage.measurements.label()` to identify individual blobs in the heatmap. 

Assuming each cluster of positive windows corresponded to a vehicle, I constructed bounding boxes to cover the area of each blob detected. After detecting the correct amount of cars, I was able to combine the positive bounding boxes into one bounding box for each car:

![one_box_per_car]

---

### Video

A link to the final video output for this project is provided below. The code pipeline performs reasonably well on the entire video.

### P5_project_video_final.mp4
https://youtu.be/Vx5GtROunzQ

<a href="http://www.youtube.com/watch?feature=player_embedded&v=Vx5GtROunzQ
" target="_blank"><img src="http://img.youtube.com/vi/Vx5GtROunzQ/0.jpg" 
alt="YouTube" width="240" height="180" border="10" /></a>

>>>>>>> CarND_P5_Vehicle_Detection_and_Tracking/master
---

### Discussion

<<<<<<< HEAD
This project was difficult in that it took a while to organize everything into a functioning system. The steps required to calibrate the camera, undistort an image and produce a thresholded binary image were straightforward. However, the perspective transform and steps following that proved to be challenging. I found the video stream was significantly dependent on the color and gradient filters applied to the images, and I had difficulty overcoming this dependancy. If my pipeline were tested on a video taken at night, I predict that it would be unable to perform correct lane detections, as the parameters I chose for the color and gradient thresholds were tailored to a video taken during the day.

### Future Plans

I feel satisfied with the results of this project. If given more time in the future, I would like to continue learning about computer vision by working on Open Source projects and extending the pipeline to other test videos:

+ I plan to build the OpenCV GameBoy Pokedex: http://www.pyimagesearch.com/2014/03/10/building-pokedex-python-getting-started-step-1-6/
+ Challenge Videos - The `challenge_video.mp4` video is an extra challenge designed to test the pipeline under somewhat trickier conditions.  The `harder_challenge.mp4` video is another challenge and is brutal!
+ Additional Tests - Eventually, I would like to take additional videos on my own and implement the project from scratch.
>>>>>>> CarND_P4_Advanced_Lane_Finding/master
=======
Firstly, The biggest challenge with this project was getting everything to work on a video stream. Due to the limitations of my laptop, a CPU, I was not able to troubleshoot the parameters as much as I would have liked, as each iteration of testing took a frustratingly long period of time. That said, I was able to find a few combinations of feature extraction parameters that performed better than others, and ultimately I realized the importance of spatial binning and HOG as two critical factors in creating a successful pipeline.

Secondly, I would also have figured out a way to smooth the vehicle detections from frame to frame. Perhaps some of my code would have run faster, and the overall output would be more desirable.

Lastly, the sliding window technique that I implemented was carried out for each frame, and HOG features were generated within each window, increasing processing time. Although I was able to produce a decent output, the code would have run faster had I run HOG features once as an array over the whole test image, then applied indexes of that array to each individual sliding window. Perhaps I will implement this concept in the future.

### Future Plans

+ **Include Additional Datasets**- I would like to implement Udacity's recently released dataset in the future. 

+ **Test Additional Classifiers**- Linear SVC was sufficient for this project, as it provided me with above 94% accuracy on a regular basis. However, if in the future I require a real-world system that must be able to classify cars on a human performance-level, I would need to experiment with other classifiers to improve past 94%.

+ **Add Lane Detection**- I would like to one day add my lane-finding algorithm from [Project 4 - Advanced Lane Detection](https://github.com/nhiddink/CarND_P4_Advanced_Lane_Finding) to perform simultaneous lane-finding and vehicle detection on a video.

+ **Test On Additional Videos**- One day I hope to implement this project on my own test videos.
>>>>>>> CarND_P5_Vehicle_Detection_and_Tracking/master
