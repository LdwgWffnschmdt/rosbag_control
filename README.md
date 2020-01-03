# rosbag_control

This package contains a node that exposes an actionlib API to control rosbag.

## Installation
```bash
# Clone this repo in your catkin workspaces src folder
cd catkin_ws/src
git clone https://github.com/LdwgWffnschmdt/rosbag_control.git

# Make the cfg file executable
chmod a+x rosbag_control/cfg/Rosbag.cfg

# Build your workspace
cd catkin_ws
catkin_make
```

## Usage
The node exposes an actionlib API:
```bash
#goal definition
string arguments
---
#result definition
---
#feedback
string stdout
string stderr
```
The node will execute ```rosbag "arguments"``` so you can run any rosbag script. To stop the script just cancel the action.

The folder in which the script is executed can be configured with dynamic_reconfigure