# Self-Balancing-Bot
It is the two wheeled robot which moves forward with balancing itself vertically straight position.

Components required: 
1.Self balancing robot chassis
2.Arduino Mega2560,Gyro sensor
3.Two Johnson motors,Motor driver
4.Two wheels
5.Wires 
6.DC Power supply(12 volt) and other material if requires.

Mechanical Structure:
The bot consists of 2 platforms which have  arduino, IMU, motor driver mounted on it. 
On the  lower part of the base platform, the two Johnson type motors (200 rpm) are clamped. 
The whole bot gets  balanced on two wheels having the required grip  providing sufficient friction (as there are large chances  for wheels to skid).(See img1_Mechanical model) 

Connections:
(See img2_connections)

How Balancing Works:
It will be prevented from falling by giving acceleration  to the wheels according to its inclination from the  vertical. If the bot gets tilts by an angle, than in the  frame of the wheels, the centre of mass of the bot will experience a pseudo force which will apply a torque  opposite to the direction of tilt.(See img3_how balancing works).

Algorithms:
(1) PID 
    The control algorithm behind maintaining it balanced on the autonomous self-balancing two wheel robot was the PID controller.The         proportional, integral, and derivative (PID) controller, is well known as a three term controller.(See img4_PIDcontroller)
    The input to the controller is the error from the system. The Kp, Ki, and Kd are referred as the proportional, integral, and             derivative constants (the three terms get multiplied by these constants respectively).
    Note: Vertical upright position is taken as reference position.
    Kp : This the term responsible for reducing the error from the upright position
    Kd : This term is responsible for the reduction of rate of change of error.
    Ki :  This term is responsible for reduction of overshoot from the reference position.
    (See img5_PIDtunnig)
    
(2) Kalman Filter
    The output of kalman filter is fed into the PID input for further processing.
    It is being used for the fusion of the outputs of the two sensors used,reduction of noise of the two sensors by taking appropriate       weightage which will vary according to time,Estimation of the optimal state using the prediction from the last stage and current         state  measurement.(See img6_Kalman filter)
    It is based on weighted average giving more weightage to the reading which is more certain and recursive process which leads to
    less memory consumption of microprocessor also gives theoretically and practically accurate data.
    
Applications:
1.Segway vehicle(see img7_segway vehicle)
2.short distance vehicles as per requirements








