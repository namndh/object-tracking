# Report
### Object tracking in Computer vision
### Nam nguyen - 07/10/2018

#### 1. Introduction:
Videos are actually sequences of images, each of which called a frame, displayed in fast enough frequency so that human eyes can percept the continuity of its content. The identificaton of regions is typically the fist step in many computer vision applications including event detection, video surveillance, and robotics. 

It is extremely difficult to properly handle unknown objects or objects with significant variations in color, shape and textures in object detection, objection tracking algorithms. An image, ussually from a video sequece, is divided into two complimentary sets of pixels; foreground objects and set of background pixels. Because of ambiguity in definition of what should be considered as foreground or background, we simply assume that moving objects like people, boats and cars are foreground objects and the remaining is the background.
    
There are some basic steps for tracking an object in a video sequence:
-   Object Detection: is to identify objects of interest in the video sequence and to cluster pixels of these objects. Common methods which are usually applied in this step are frame differencing, Optical Flow or Background Subtraction.
-   Object Classification: in this step, we classify detected objects into different classes. The approaches to this step are Shape-based classification, Motion-based classification, Color-based or texture-based classification.
-   Object Tracking: The problem of approximating the path of an object in the image plane as it moves around a scence. The approachs to track the objects are point tracking, kernel tracking and sulhouette

This report is structured in the following way: Sect.1 gives introduction to object tracking, Sect.2 describes object tracking methods.
#### 2. Object Tracking methods:
The aim of object tracking is to create the route for an object over time finding its position in video sequences. In the first stage, Region of Interest in each frame is achieved by means of an object detection algorithm, and then tracking corresponds to object across frames. In final stage, the object region is projected by iteratively updating object location obtained from previous frames. Object tracking can be classified as point tracking, kernel based tracking and silhouette based tracking.
##### 2.1 Point tracking:
Tracking can be formulated as the correspondence of detected objects represented by points across frames. Point correspondence is a complicated problem - mainly in the existence of occlusions, misdetections, entries and exits of objects. Overall, point correspondence methods can be devicded into two broad categories, namely, deterministic and statistical appoaches. The deterministic methods use qualitative motion heuristics to constrain the correspondence problem. On the other hand, statistical or probabilistic methods explicitly take the object measurement and take uncertainties into account to establish correspondences. 