[//]: # (Image References)

[image1]: ./misc/rover_image.jpg
[image2]: ./calibration_images/example_grid1.jpg
[image3]: ./calibration_images/example_rock1.jpg 


### Notebook Analysis
#### 1. Run the functions provided in the notebook on test images (first with the test data provided, next on data you have recorded). Add/modify functions to allow for color selection of obstacles and rock samples.
-  To detect rocks in an image I had to implement a function to detect the rock’s color in the image which in our project is yellow. To find yellow pixels I look for pixels with high levels of RED and GREEN and low level of BLUE.
 
![alt text][image1]

#### 1. Populate the `process_image()` function with the appropriate analysis steps to map pixels identifying navigable terrain, obstacles and rock samples into a worldmap.  Run `process_image()` on your test data using the `moviepy` functions provided to create video output of your result. 
-After reading every new image the we have to take the following steps to analysis the image and determine the navigable path, obstacles, and rock samples.
       1) Define source and destination points for perspective transform.
       2) Apply perspective transform.
       3) Apply color threshold to identify navigable terrain/obstacles/rock samples,here we get the location of pixels in the image plane.
       4) Convert Image plane location to rover-centric location.
       5)  To calculate the fidelity and map the world we have to Convert rover-centric pixel values to world coords.
       6) Update worldmap.
       7) After this we can use the information to make decision and also display.

![alt text][image2]
### Autonomous Navigation and Mapping

#### 1. Fill in the `perception_step()` (at the bottom of the `perception.py` script) and `decision_step()` (in `decision.py`) functions in the autonomous mapping scripts and an explanation is provided in the writeup of how and why these functions were modified as they were.
-Basicly copied the same fucntion in the notebook to perception.py.

#### 2. Launching in autonomous mode your rover can navigate and map autonomously.  Explain your results and how you might improve them in your writeup.
The rover is able to navigate and fulfill the minimum requiment but my goal is to change the decission_step() so the rover can navigate to a specefic loction in the world map.

**Note: running the simulator with different choices of resolution and graphics quality may produce different results, particularly on different machines!  Make a note of your simulator settings (resolution and graphics quality set on launch) and frames per second (FPS output to terminal by `drive_rover.py`) in your writeup when you submit the project so your reviewer can reproduce your results.**

Here I'll talk about the approach I took, what techniques I used, what worked and why, where the pipeline might fail and how I might improve it if I were going to pursue this project further.
I use all the guid line in the walkthrough video as I was really late hope to catch-up soon.



![alt text][image3]


