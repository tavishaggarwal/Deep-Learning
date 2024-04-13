# Detecting vehicles in video

Before any road construction, the government needs to determine the width and strength of the road, along with numerous other factors. These factors are determined by counting and categorising the vehicles that would run on the road once it's built. Earlier, manual surveys were conducted by counting the number of vehicles passing through the lane and categorising vehicles as a car, a truck, etc. 

This solution will help goverment to automate this process.

## Approach

Approach to develop a solution is divided into two parts. First one is to detect the vehicle and second part is to classify the vehicles.

<img src="Detecting vehicle in video - Tracking, Identification, and Classification/vehicle_detection.png" alt="Approach for Detecting vehicles in video">

### Vehicle detection:

- The first step is to break a video into individual frames.
- Then, make an imaginary (virtual) line across the lane.
- To keep the track of the vehicles, increase the vehicle count by one whenever a vehicle crosses the imaginary line.
 

### Vehicle classification:

- Crop the vehicle that just passed the imaginary line.
- Classify the cropped vehicle using a CNN classifier.


## Directory Structure
- Detecting vehicle in video - Preprocessing
    - 1. Detecting vehicles in video - pre-processing notebook.ipynb
    - 2. Understanding tracking of the object.ipynb
- Detecting vehicle in video - Tracking, Identification, and Classification
    - 3. Tracking and Identification of vehicles.ipynb
    - 4. Vehicle Classification.ipynb

First notebook is a prerequisites to understand how to compare two frames and find the blobs from the frames. Second notebook demonstrates a pseudo code that is used to track the vehicles so that one vehicle is not counted twice or more.

Third notebook is where vehicle identification tracking is happeing and finlly fourth notebook is where we are classifying tracked vehicle into 2/3 wheelers, 4 wheelers, and more-than-4 wheelers.