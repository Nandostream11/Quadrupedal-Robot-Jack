# H/ware branch of Quadrupedal Robot

The hardware consists of 12 Servo Motors providing each of the 4 leg-tips with 3-Dof acccounting for a total of 12 DoFs Quadrupedal Robot.
Brain- Raspberry Pi 4.0 B
Controller- Arduino Mega256
Servo Driver module
IMU-BNO055 Sensor(9-axis)
LIDAR- RP LiDAR A1

Look into rpi_cmds.txt for setup commands/instructions

Setup and soyurce the workspace:-
```bash
cd <quad_ws>
source install/setup.bash
```
1. Launch the hardware interfaces:
```bash
ros2 launch quadruped_description hardware.launch.py
```
2. Launch the joystick command interface
```bash
# ros2 launch quadruped_description joystick.launch.py #now merged wth hardware.launch.py
```
3. Run the bezier trajectory follower-controller
```bash
ros2 run quadruped_description traj_bezier
```
4. See the BNO055 IMU data:
```bash
ros2 run ros2_bno055 bno055
```
5. Initialize the LiDAR Pointcloud feed:
```bash
ros2 launch sllidar_ros2 view_sllidar_a1_launch.py
```
