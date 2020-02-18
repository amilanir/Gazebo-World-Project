# Gazebo-World-Project

In this project I designed a Gazebo World environment by including multiple models to include an office space and robots. A cuatomized plugin is written to interact with the gazebo world.

1. Build a single floor wall structure using the Building Editor tool in Gazebo. Apply at least one feature, one color, and optionally one texture to your structure. Make sure there's enough space between the walls for a robot to navigate.
2. Model any object of your choice using the Model Editor tool in Gazebo. Your model links should be connected with joints.
3. Import your structure and two instances of your model inside an empty Gazebo World.
4. Import at least one model from the Gazebo online library and implement it in your existing Gazebo world.
5. Write a C++ World Plugin to interact with your world. Your code should display “Welcome to ’s World!” message as soon as you launch the Gazebo world file.

## Directory Structure
```
    .Project1                             # Build My World Project 
       ├── model                          # Model files 
       │   ├── Building
       │   │   ├── model.config
       │   │   ├── model.sdf
       │   ├── HumanoidRobot
       │   │   ├── model.config
       │   │   ├── model.sdf
       ├── script                         # Gazebo World plugin C++ script      
       │   ├── welcome_message.cpp
       ├── world                          # Gazebo main World containing models 
       │   ├── UdacityOffice.world
       ├── CMakeLists.txt                 # Link libraries 
       └──                                                         
```

## Steps to launch the simulation

### Step 1 Update and upgrade the Workspace image
```sh
$ sudo apt-get update && sudo apt-get upgrade -y
```

### Step 2 Clone the lab folder in /home/workspace/
```sh
$ cd /home/workspace/
$ git clone https://github.com/amilanir/Gazebo-World-Project/
```

### Step 3 Compile the code
```sh
$ cd /home/workspace/Gazeb0-World-Project/
$ mkdir build
$ cd build/
$ cmake ../
$ make
```

### Step 4 Add the library path to the Gazebo plugin path  
```sh
$ export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:/home/workspace/Gazebo-World-Project/build
```

### Step 5 Run the Gazebo World file  
```sh
$ cd /home/workspace/Gazebo-World-Project/world/
$ gazebo myofficeworld
```

### Output
The cutomize welcome  message will be displayed and the robot inside a Gazebo office world will launch as shown below. 

![Overview](/media/Amila's_Office.png) 

    
 

