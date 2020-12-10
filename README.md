# Object Tracking for Safety - Team SafeBots

[EECS 504] Final Project - Saptadeep Debnath, Preeti Kannapan, Malvika Shetty

The aim of our project is to implement object tracking in videos using bounded boxes for safety applications. With more and more autonomous robots and vehicles being deployed in the world, it is becoming increasingly important to ensure the safety of everyone in the robot’s environment. There are many contexts in which this is applicable – i) human-robot interactions e.g. collaborative robots ii) robot-robot interactions e.g. industrial robots iii) robot-object interactions e.g. in manipulation or obstacle avoidance tasks. Specifically, we would like to use object tracking to detect and draw conclusions about the distance of the moving object from the camera, and additionally issue a warning based on the proximity of the object to the camera. Such a warning would be useful for a robot, vehicle, or even human, to react appropriately when the camera is mounted on them. This will be done with a depth estimator method that makes use of the variation in scale of the bounding box with depth of the object. Therefore, we propose to implement object tracking as well as a proximity warning system for safety purposes.

## Goals
The video submission will include (but will not be limited to);
- the methodology used to implement object detection and tracking,
- a comparative study of the implemented method with other state-of-the-art techniques, 
- the methodology used to implement the proximity warning system with depth estimation, and
- a live visualization of the integrated system performing object tracking and proximity warning on a video.


## Dependencies

1. Download sensor data and groundtruth.csv from the [NCLT dataset](http://robots.engin.umich.edu/nclt/) for a date, save all csv files in one folder named by the date, and store the folder in `/data`.

2. Run the script `/utils/read_data_and_convert_to_mat.py` 

## Running the code
1. `/src/LIEKF_example.m` runs the Left-Invarriant EKF on the NCLT, and compares with ground truth.
2. `/src/madgwick_example.m` runs the Madgwick algorithm.
3. `/src/EKF_example.m` runs the Extended Kalman Filter on the NCLT, and compares with ground truth.
4. `/src/LIEKF_example_wbias.m` runs the Left-Invariant EKF including IMU bias on the NCLT, and compares with ground truth.

`/src/LIEKF_example.m`, `src/LIEKF_example_wbis.m` and `/src/EKF_example.m` produces three plots; planned robot trajectory compared with the ground truth, comparison of the computed euler angles with the ground truth and Mahalanobis distances for the predicted robot states.

## Results

Plot generated 

<!-- ![alt-text](/report/ekf.gif) -->



Check the [proposal](https://github.com/team16-mobrob-w20/inekf-localization/blob/master/EECS568_Team16_proposal.pdf), [final report](https://github.com/team16-mobrob-w20/inekf-localization/blob/master/EECS568_Team16_Report.pdf) and [video presentation](https://youtu.be/aILSsw7K2z8) for more details on implementation. 



## Team Members
- [Saptadeep Debnath](https://www.linkedin.com/in/saptadeep-deb/) (saptadeb@umich.edu)
- [Preeti Kannapan](https://www.linkedin.com/in/preeti-kannapan-646663170) (preetimk@umich.edu)
- [Malvika Shetty](https://www.linkedin.com/in/malvikadshetty) (malvikad@umich.edu)
