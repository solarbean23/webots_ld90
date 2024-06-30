# webots_ld90

# Run Webots
ros2 launch webots_ros2_ld90 robot_launch.py world:=no_human.wbt
other maps: modify_no_human.wbt , contest.wbt

# Run Rviz2
ros2 run rviz2 rviz2 -d $(ros2 pkg prefix nav2_bringup)/share/nav2_bringup/rviz/nav2_default_view.rviz

# SLAM
ros2 launch nav2_bringup bringup_launch.py params_file:=webots_ros2_ld90/resource/nav2_params.yaml map:=my_map.yaml slam:=True 

# Nav2
ros2 launch nav2_bringup bringup_launch.py params_file:=webots_ros2_ld90/resource/nav2_params.yaml map:=test_map2.yaml
