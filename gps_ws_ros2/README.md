# Info
Ros version: dashing-diademata (ros2)
# Setup
:~simplertk2b/gps\_ws\_ros2$ colcon build

It is important that the shared object library is in one of the folders that is part of LD\_LIBRARY\_PATH (do echo $LD\_LIBRARY\_PATH to see the files in this volder)
:~simplertk2b/gps\_ws\_ros2$ cp src/simplertk2b/lib/libgps.so /opt/ros/dashing/lib

# Run
sudo su
:~simplertk2b/gps\_ws\_ros2$ source /opt/ros/dashing/setup.bash
:~simplertk2b/gps\_ws\_ros2$ . install/local\_setup.bash
:~simplertk2b/gps\_ws\_ros2$ ros2 run simplertk2b\_node simplertk2b\_node

# run without the need of using sudo
add yourself to the group dialout
sudo usermod -a -G dialout MY_USER_NAME
cfr. https://unix.stackexchange.com/questions/14354/read-write-to-a-serial-port-without-root
--> did not work: solution
ls /dev/ | grep "ACM"
sudo chmod 666 /dev/ttyACM0 /dev/ttyACM1

