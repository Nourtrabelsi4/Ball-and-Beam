# Ball-and-Beam
Introduction:
The ball and beam balance system is one of the most popular laboratory controls design experiments because it is very simple to understand and can be used to study the implementation of classical and modern control techniques.The Ball and Beam module is ideal to introduce various control concepts related to unstable closed-loop systems since such systems can prove dangerous to test in the real world.

Objectif:
This project covers:

Creation of avalid model of the system.
Identification of numerical values for the model parameters.
Assembling the system hardware, and implementing the control system using a microcontroller to interface with the motor.
A PID controller is used to control the position of the ball on the beam.

Physical Setup:
A ball is placed on a beam, see figure "Benchmark.png", where it is allowed to roll with one degree of freedom along the length of the beam. A lever arm is attached to the beam at one end and a servo gear at the other. As the servo gear turns by an angle theta, the lever changes the angle of the beam by alpha.

Mechanical Part
Custom 3D printed parts made with SolidWorks. Base support + Beam  + Servo motor horn + Lever_arm + Ping pong ball

Electrical Part
You will need: Arduino(Uno), Servo_motor, Ultrasonic sensor, jumper wires and Battery

Software programming description:
At the beginning, the system receives the ball position from ultrasonic distance sensor and compares it with the desired distance which can be set by the user “the set point”. If they are equal than the system maintains the ball in the desired position. Otherwise the system have to acquire data from the sensor, filtering it than computing the error and apply the PID control signal to the DC servomotor which rotate to change the ball position and so on until we obtain the equilibrium position of the ball. You can see haw we translate all this description on a VI simulation (BallAndBeam.vi)
