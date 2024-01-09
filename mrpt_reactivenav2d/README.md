# mrpt_reactivenav2d

## Overview
This package provides a ROS 2 node for reactive navigation for wheeled robots
using MRPT navigation algorithms (TP-Space).

## How to cite

<details>
  <summary>Main papers</summary>

  IROS06 ([PDF](https://ingmec.ual.es/~jlblanco/papers/blanco2006tps_IROS.pdf))
  ```bibtex
  @INPROCEEDINGS{,
       author = {Blanco, Jos{\'{e}}-Luis and Gonz{\'{a}}lez-Jim{\'{e}}nez, Javier and Fern{\'{a}}ndez-Madrigal, Juan-Antonio},
        month = oct,
        title = {The Trajectory Parameter Space (TP-Space): A New Space Representation for Non-Holonomic Mobile Robot Reactive Navigation},
        booktitle = {IEEE International Conference on Intelligent Robots and Systems (IROS'06)},
        year = {2006},
        location = {Beijing (China)}
  }
  ```

</details>

<details>
  <summary>Other related papers</summary>

  [IEEE RAM 2023](https://ieeexplore.ieee.org/abstract/document/10355540/)
  ```bibtex
  @ARTICLE{xiao2023barn,
      author = {Xiao, Xuesu and Xu, Zifan and Warnell, Garrett and Stone, Peter and Gebelli Guinjoan, Ferran and T Rodrigues, Romulo and Bruyninckx, Herman and Mandala, Hanjaya and Christmann, Guilherme and Blanco, Jos{\'{e}}-Luis and Somashekara Rai, Shravan},
       month = {{aug}},
       title = {Autonomous Ground Navigation in Highly Constrained Spaces: Lessons learned from The 2nd BARN Challenge at ICRA 2023},
       journal = {IEEE Robotics & Automation Magazine},
       volume = {30},
       number = {4},
       year = {2023},
       url = {https://ieeexplore.ieee.org/abstract/document/10355540/},
       doi = {10.1109/MRA.2023.3322920},
       pages = {91--97}
  }
  ```

  IJARS 2015 [PDF](https://ingmec.ual.es/~jlblanco/papers/blanco2015tps_rrt.pdf)
  ```bibtex
  @ARTICLE{bellone2015tprrt,
      author = {Blanco, Jos{\'{e}}-Luis and Bellone, Mauro and Gim{\'{e}}nez-Fern{\'{a}}ndez, Antonio},
      month = {{{may}}},
      title = {TP-Space RRT: Kinematic path planning of non-holonomic any-shape vehicles},
      journal = {International Journal of Advanced Robotic Systems},
      volume = {12},
      number = {55},
      year = {2015},
      url = {http://www.intechopen.com/journals/international_journal_of_advanced_robotic_systems/tp-space-rrt-ndash-kinematic-path-planning-of-non-holonomic-any-shape-vehicles},
      doi = {10.5772/60463}
  }
  ```

</details>


## Configuration

The main **parameters** of our approach are:

- **Robot shape**: The "2D foot-print" of the robot.
- **PTGs**: One or more families of trajectories, used to look ahead and plan what is the most interesting next motor command.
- **Motion decision**: These parameters can be tuned to modify the heuristics that control what motor actions are selected.

## Demos

### Navigation in simulated warehouse

    ros2 launch mrpt_tutorials reactive_nav_demo_with_mvsim.launch.py

to start:

* ``mrpt_reactivenav2d`` for the autonomous reactive navigation (this package),
* ``mrpt_pointcloud_pipeline`` for generating input obstacles for the navigator from lidar data,
* ``mvsim`` to simulate a live robot that can be controlled by the navigator.

## Node: mrpt_reactivenav2d_node

### Working rationale

The C++ ROS 2 node comprises XXX


### ROS 2 parameters

XXX

### Subscribed topics
* xxx

### Published topics
* xxx

### Template ROS 2 launch files

This package provides [launch/reactivenav.launch.py](launch/reactivenav.launch.py):

    ros2 launch mrpt_reactivenav2d reactivenav.launch.py

which can be used in user projects to launch the MRPT reactive navigation node, by setting these [launch arguments](https://docs.ros.org/en/rolling/Tutorials/Intermediate/Launch/Using-Substitutions.html):

* ``XXX_config_file``: Path to an INI file with...

