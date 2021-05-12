# Gazebo maps
Self-made Gazebo maps for public

<br>

## List
+ small-scale maze environment
+ large-scale mine environment - edited from [MBPlanner](https://github.com/ntnu-arl/mbplanner_ros/tree/master/planner_gazebo_sim/worlds)
+ maze with height map (hills) environment

<br>

## How to use
+ Clone the git, add the folder in `GAZEBO_MODEL_PATH`
+ Add `common models` to environment first
~~~shell
$ git clone https://github.com/engcang/gazebo_maps
$ echo "export GAZEBO_MODEL_PATH=$GAZEBO_MODEL_PATH:$(pwd)/gazebo_maps/common_models" >> ~/.bashrc
~~~

+ (Optional) add the wanted world to environment
~~~shell
$ echo "export GAZEBO_MODEL_PATH=$GAZEBO_MODEL_PATH:$(pwd)/gazebo_maps/height_maze" >> ~/.bashrc

$ echo "export GAZEBO_MODEL_PATH=$GAZEBO_MODEL_PATH:$(pwd)/gazebo_maps/small_maze" >> ~/.bashrc

$ echo "export GAZEBO_MODEL_PATH=$GAZEBO_MODEL_PATH:$(pwd)/gazebo_maps/large_mine_abandoned" >> ~/.bashrc

$ source ~/.bashrc
~~~

+ launch the `world`
~~~shell
$ roslaunch gazebo_ros empty_world.launch world_name:=$(pwd)/gazebo_maps/height_maze/quad.world
or
$ roslaunch gazebo_ros empty_world.launch world_name:=$(pwd)/gazebo_maps/small_maze/smaze2d.world
or
$ roslaunch gazebo_ros empty_world.launch world_name:=$(pwd)/gazebo_maps/large_mine_abandoned/lcmine.world
~~~
