# CarND-Path-Planning-Project 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

## Overview  
---
In this project your goal is to safely navigate around a virtual highway with other traffic that is driving +-10 MPH of the 50 MPH speed limit. You will be provided the car's localization and sensor fusion data, there is also a sparse map list of waypoints around the highway.

## Description  
---
- The code compiles correctly
- The car is able to drive at least 4.32 miles without incident
- The car drives according to the speed limit
- Max Acceleration and Jerk are not Exceeded
- Car does not have collisions
- The car stays in its lane, except for the time between changing lanes
- The car is able to change lanes
- There is a reflection on how to generate paths


## Using Library
---
- [JSON for Modern C++](https://github.com/nlohmann/json)  
  Template header library for connecting in JSON format

- [uWebSockets](https://github.com/uNetworking/uWebSockets)  
  This is dynamic library for communicating with Term2.
  To communicate with Term2, you need to compile something with a specific commit ID, and you can build your environment with the following command:

  ```
  ./install-ubuntu.sh
  ```
- [Cubic Spline interpolation in C++](https://kluge.in-chemnitz.de/opensource/spline/)
  

## Basic Build And Run Instructions
---
Enter the command in the top directory of the project according to the following procedure.  

1. Compile the edited code  
    1. mkdir build  
    1. cd build  
    1. cmake ..  
    1. make  
    1. ./path_planning  

    Alternatively some scripts have been included to streamline this process, these can be leveraged by executing the following in the top directory of the project:      
    1. ./clean.sh
    1. ./build.sh
    1. ./run.sh
1. Start Term3 Simulator

## Requirement
---
### Environment for starting an Path Planning Project
- cmake >= 3.5
  - All OSes: [click here for installation instructions](https://cmake.org/install/)
- make >= 4.1
  - Linux: make is installed by default on most Linux distros
  - Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  - Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
- gcc/g++ >= 5.4
  - Linux: gcc / g++ is installed by default on most Linux distros
  - Mac: same deal as make - [install Xcode command line tools]((https://developer.apple.com/xcode/features/)
  - Windows: recommend using [MinGW](http://www.mingw.org/)
- [uWebSockets](https://github.com/uWebSockets/uWebSockets)
  - Run either `install-mac.sh` or `install-ubuntu.sh`.
  - If you install from source, checkout to commit `e94b6e1`, i.e.
    ```
    git clone https://github.com/uWebSockets/uWebSockets 
    cd uWebSockets
    git checkout e94b6e1
    ```

### Simulator.
You can download the Term3 Simulator which contains the Path Planning Project from the [releases tab (https://github.com/udacity/self-driving-car-sim/releases/tag/T3_v1.2).  

To run the simulator on Mac/Linux, first make the binary file executable with the following command:
```shell
sudo chmod u+x {simulator_file_name}
```

## Communication protocol with the simulator  
---
Here is the main protocol that main.cpp uses for uWebSocketIO in communicating with the simulator.  

### The map of the highway is in data/highway_map.txt  
Each waypoint in the list contains  [x,y,s,dx,dy] values. x and y are the waypoint's map coordinate position, the s value is the distance along the road to get to that waypoint in meters, the dx and dy values define the unit normal vector pointing outward of the highway loop.

The highway's waypoints loop around so the frenet s value, distance along the road, goes from 0 to 6945.554.

### Main car's localization Data (No Noise)  
["x"] The car's x position in map coordinates  
["y"] The car's y position in map coordinates  
["s"] The car's s position in frenet coordinates  
["d"] The car's d position in frenet coordinates  
["yaw"] The car's yaw angle in the map  
["speed"] The car's speed in MPH  

### Previous path data given to the Planner  
["previous_path_x"] The previous list of x points previously given to the simulator  
["previous_path_y"] The previous list of y points previously given to the simulator  

### Previous path's end s and d values  
["end_path_s"] The previous list's last point's frenet s value  
["end_path_d"] The previous list's last point's frenet d value  

### Sensor Fusion Data, a list of all other car's attributes on the same side of the road. (No Noise)  
["sensor_fusion"] A 2d vector of cars and then that car's [car's unique ID, car's x position in map coordinates, car's y position in map coordinates, car's x velocity in m/s, car's y velocity in m/s, car's s position in frenet coordinates, car's d position in frenet coordinates.  

## Submission  
---
- [writeup.md](./writeup.md)
- [main.cpp](./src/main.cpp)

## Code Style  
---
Please (do your best to) stick to [Google's C++ style guide](https://google.github.io/styleguide/cppguide.html).

## Licence
---
[MIT](LICENSE)

## Author
---
[kumab2221](https://github.com/kumab2221)