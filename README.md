[![Udacity - Robotics NanoDegree Program](https://s3-us-west-1.amazonaws.com/udacity-robotics/Extra+Images/RoboND_flag.png)](https://www.udacity.com/robotics)

# Udacity Nanodegree: Robotics Software Engineer

## Project 02: Go Chase It!

<p align="center">
    <img src="./docs/Gazebo_demo.mp4" width="600" height="338" title="Go Chase It!" >
</p>

### D

.go_chase_it                              # Project 02: Go Chase It!
├── docs
│   ├── Gazebo_demo.mp4
│   └── RViz_demo.mp4
├── LICENSE
├── my_ball
│   ├── model.config
│   └── model.sdf
├── README.md
└── src
    ├── ball_chaser                      # ball_chaser package
    │   ├── CMakeLists.txt
    │   ├── include
    │   │   └── ball_chaser
    │   ├── launch
    │   │   └── ball_chaser.launch
    │   ├── package.xml
    │   ├── src
    │   │   ├── drive_bot.cpp            # Robot driver node
    │   │   └── process_image.cpp        # Image processing node
    │   └── srv
    │       └── DriveToTarget.srv
    ├── CMakeLists.txt -> /opt/ros/kinetic/share/catkin/cmake/toplevel.cmake
    └── my_robot
        ├── CMakeLists.txt
        ├── launch
        │   ├── robot_description.launch
        │   └── world.launch
        ├── meshes
        │   └── hokuyo.dae
        ├── package.xml
        ├── urdf
        │   ├── my_robot.gazebo
        │   └── my_robot.xacro
        └── worlds
            ├── empty.world
            └── my_world.world        # World file   



### How to run

#### 1. First of all, clone this repo:
```
git clone https://github.com/Suraj0712/Build_my_world.git
```

#### 2. Launch the robot inside your world
This can be done by launching ```world.launch``` file:
```
$ cd <directory_where_you_have_cloned_the_repo>/go_chase_it/
$ catkin_make
$ source devel/setup.bash
$ roslaunch my_robot world.launch
```

#### 3. Run ``` drive_bot ``` and ``` process_image ```
This can be done by launching ```ball_chaser.launch``` file:
```
$ cd <directory_where_you_have_cloned_the_repo>/go_chase_it/
$ source devel/setup.bash
$ roslaunch ball_chaser ball_chaser.launch
```

#### 4. Visualize
To visualize the robot’s camera images, you can subscribe to camera RGB image topic from RViz. Or you can run the rqt_image_view node:
```
$ cd <directory_where_you_have_cloned_the_repo>/go_chase_it/
$ source devel/setup.bash
$ rosrun rqt_image_view rqt_image_view
```

Now, put the white ball at different positions in front of the robot to see how robot moves to chase the white ball!

<p align="center">
    <img src="./docs/RViz_demo.mp4" width="600" height="338" title="Go Chase It!" >
</p>
