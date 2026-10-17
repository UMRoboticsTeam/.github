# University of Manitoba Robotics Team
The University of Manitoba Robotics Team ([UMRT](https://umrt.ca)) is a design team of undergraduate students, primarily from Computer, Electrical, and Mechanical Engineering as well as Computer Science, who design a mars-style rover for the [Canadian International Rover Challenge](https://circ.cstag.ca/).

The team is divided into 6 sections:
- **Embedded**, which deals with the software running on the rover and drive-by-wire system.
- **Communications-Operations**, which deals with the communication link between the rover and base station, as well as base station design and operation.
- **Electrical**, which deals with the electrical architecture of the rover and the battery system.
- **Chassis**, which deals with the mechanical design of the rover body.
- **Robotic Arm**, which deals with the design of the robotic arm system used for manipulating the environment.
- **Mission Control**, which deals with mission strategy, planning, and simulation.

## Repositories

The rover software system is split into many different Git repositories, each responsible for a particular portion of the system.
Generally, each repository is "owned" by one of the above sections. Some repositories listed important for all sections. Repositories not currently in use are listed at the bottom.

### Intersectional

Out of this set, `umrt-build` is the most important repository.

| Repository                                                               | Description                                                                              | Status  |
| ------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------- | ------- |
| [umrt-build](https://github.com/UMRoboticsTeam/umrt-build)               | Docker image containing all dependencies needed to build UMRT software packages          | Current |
| [umrt-template-ros](https://github.com/UMRoboticsTeam/umrt-template-ros) | Template for UMRT ROS project repositories                                               | Current |
| [umrt-template](https://github.com/UMRoboticsTeam/umrt-template)         | Template for general UMRT Git repositories                                               | Current |
| [umrt-ci-cd](https://github.com/UMRoboticsTeam/umrt-ci-cd)               | Continuous integration/development workflows for the UMRT build system and PR management | Current |
| [umrt-apt-image](https://github.com/UMRoboticsTeam/umrt-apt-image)       | Docker image containing tools for managing UMRT's internal debian repository             | Current |


### Robotic Arm

Out of this set, `umrt-arm-ros-firmware` is the most important repository. The `ros2_j1939_babbler`, or just "the babbler" is also a very important package for our workflow, but it is complete and mostly just needs to be maintained.

| Repository                                                                                 | Description                                                                                    | Status      |
| ------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------- | ----------- |
| [umrt-arm-ros-firmware](https://github.com/UMRoboticsTeam/umrt-arm-ros-firmware)           | ROS software for controlling the arm via ros2_control                                          | Current     |
| [umrt-arm-firmware-lib](https://github.com/UMRoboticsTeam/umrt-arm-firmware-lib)           | C++ library for controlling the arm's stepper motors from the high-level computer              | Current     |
| [umrt-arm-encoder-driver](https://github.com/UMRoboticsTeam/umrt-arm-encoder-driver)       | C++ library for interpreting the CAN messages published by the arm's rotary encoders           | Current     |
| [umrt-arm-encoder-ros](https://github.com/UMRoboticsTeam/umrt-arm-encoder-ros)             | ROS software for publishing the data received from the arm's rotary encoders. Not implemented. | Current     |
| [umrt-arm-joystick-operator](https://github.com/UMRoboticsTeam/umrt-arm-joystick-operator) | ROS node for using a joystick with the arm. Including realtime control.                        | Current     |
| [ros2_j1939_babbler](https://github.com/UMRoboticsTeam/ros2_j1939_babbler)                 | A custom ROS-based J1939-to-ROS converter that can tranform any CAN message from a DBC file.   | Maintenance |
| [ros2_j1939_babbler_msgs](https://github.com/UMRoboticsTeam/ros2_j1939_babbler_msgs)       | A package template for creating messages for `ros2_j1939_babbler` to use.                      | Maintenance |


### Embedded

| Repository                                                                                                       | Description                                       | Status  |
| ---------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- | ------- |
| [umrt-ros-poe-cam](https://github.com/UMRoboticsTeam/umrt-ros-poe-cam)                                           | ROS Package for the PoE Camera                    | Current |
| [umrt-serial-cam-ros](https://github.com/UMRoboticsTeam/umrt-serial-cam-ros)                                     | ROS Package for the Serial Cameras                | Current |
| [umrt-emb-imu-driver](https://github.com/UMRoboticsTeam/umrt-emb-imu-driver)                                     | C++ Library for the IMU                           | Current |
| [umrt-emb-imu-ros](https://github.com/UMRoboticsTeam/umrt-emb-imu-ros)                                           | ROS Package for the IMU                           | Current |
| [umrt-geiger-driver](https://github.com/UMRoboticsTeam/umrt-geiger-driver)                                       | C++ Library for the Geiger Counter                | Current |
| [umrt-emb-geiger-ros](https://github.com/UMRoboticsTeam/umrt-emb-geiger-ros)                                     | ROS Package for the Geiger Counter                | Current |
| [umrt-can-ppm-gateway](https://github.com/UMRoboticsTeam/umrt-can-ppm-gateway/tree/firmware) (`firmware` branch) | MPLAB X files for the custom CAN-PPM gateway PCB. | Current |


### Electrical

Most of electrical's other files are stored in RapidHarness or Onshape.

| Repository                                                                                                       | Description                                     | Status  |
| ---------------------------------------------------------------------------------------------------------------- | ----------------------------------------------- | ------- |
| [umrt-can-ppm-gateway](https://github.com/UMRoboticsTeam/umrt-can-ppm-gateway/tree/hardware) (`hardware` branch) | KiCad files for our custom CAN-PPM gateway PCB. | Current |


### Comm-Ops

| Repository                                                             | Description                             | Status  |
| ---------------------------------------------------------------------- | --------------------------------------- | ------- |
| [umrt-com-antenna](https://github.com/UMRoboticsTeam/umrt-com-antenna) | ROS Package for the comms antenna stand | Current |

### Exec/Outreach

| Repository                                                                                           | Description                                                                                                     | Status  |
| ---------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | ------- |
| [umrt-outreach-robotcar-wireless](https://github.com/UMRoboticsTeam/umrt-outreach-robotcar-wireless) | Outreach Arduino showcase program for the Elegoo Smart Robot Car Kit v4.0 with wireless camera feed and control | Current |
| [umrt-website](https://github.com/UMRoboticsTeam/umrt-website)                                       | Official website built with Nuxt and Vue.js, hosted at [umrt.ca](https://umrt.ca/)                              | Current |
| [Outreach-RobotCar-Template](https://github.com/UMRoboticsTeam/Outreach-RobotCar-Template)           | Outreach Arduino bot used for sumo bot fights                                                                   | Current |

## Defunct / Not in use repositories

These are kept separate to not clutter the above list.

### Intersectional

| Repository                                                                       | Description                                                                                                                                                                                                                                                                                                                   | Status     |
| -------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| [umrt-design-documents](https://github.com/UMRoboticsTeam/umrt-design-documents) | Internal LaTeX documentation covering general system topics                                                                                                                                                                                                                                                                   | Not in use |
| [ros_buildfarm](https://github.com/UMRoboticsTeam/ros_buildfarm)                 | Fork of [ros-infrastructure/ros_buildfarm](https://github.com/ros-infrastructure/ros-buildfarm) that has been modified to support running in a Docker container. Was developed as part of an investigation into the CI/CD system, but was abandoned due to poor build performance and inconvenient configuration requirements | Not in use |


### Robotic Arm

| Repository                                                                                     | Description                                                                                                                                                                                                                                                         | Status     |
| ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| [arm-microcontroller-firmware](https://github.com/UMRoboticsTeam/arm-microcontroller-firmware) | Arduino program for low-level control of Prairie Pioneer's stepper motors                                                                                                                                                                                           | Not in use |
| [arm-documentation](https://github.com/UMRoboticsTeam/arm-documentation)                       | Internal LaTeX documentation and training materials covering various topics related to the arm                                                                                                                                                                      | Not in use |
| [openFrameworksArduino](https://github.com/UMRoboticsTeam/openFrameworksArduino)               | Fork of [NeuroRoboticTech/openFrameworksArduino](https://github.com/NeuroRoboticTech/openFrameworksArduino) for integration into the build system, used by umrt-arm-firmware-lib for communication with the Arduino used for Prairie Pioneer's motor control system | Not in use |


### Embedded

| Repository                                                                                     | Description                    | Status     |
| ---------------------------------------------------------------------------------------------- | ------------------------------ | ---------- |
| [umrt-ros](https://github.com/UMRoboticsTeam/umrt-ros)                                         | Monorepo for Prarie Pioneer    | Not in use |
| [umrt-stm](https://github.com/UMRoboticsTeam/umrt-stm)                                         |                                | Not in use |
| [umrt-drivetrain-ros](https://github.com/UMRoboticsTeam/umrt-drivetrain-ros)                   | ROS Pacakge for the Drivetrain | Not in use |
| [oak-poe-rtsp-autoboot](https://github.com/UMRoboticsTeam/oak-poe-rtsp-autoboot)               |                                | Not in use |
| [embedded-controller-firmware](https://github.com/UMRoboticsTeam/embedded-controller-firmware) |                                | Not in use |


### Comm-Ops

| Repository                                                                             | Description                                                      | Status     |
| -------------------------------------------------------------------------------------- | ---------------------------------------------------------------- | ---------- |
| [umrt-foxglove-collection](https://github.com/UMRoboticsTeam/umrt-foxglove-collection) | Collection of custom Foxglove UI extensions used on base station | Not in use |
| [umrt-base-station](https://github.com/UMRoboticsTeam/umrt-base-station)               | Docker image used on base station                                | Not in use |
