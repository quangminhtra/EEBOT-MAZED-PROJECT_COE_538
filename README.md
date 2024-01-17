# EEBOT-MAZED-PROJECT_COE_538
Our team's COE538 project for this year was programming the Eebot a navigation system, enabling it to complete a maze, reverse its path, and retrace its steps. The maze, illustrated in Figure 1, serves as the map for this project.

![Screenshot 2024-01-16 210352](https://github.com/quangminhtra/EEBOT-MAZED-PROJECT_COE_538/assets/130938825/3480453e-20c2-45e5-8fb3-e2a1a46883a7)

Robot Path
Starting at the entry point, the robot followed the guidance line. The guidance algorithm used the sensors at the bottom of the eebot to move the robot forward while keeping the line in the middle. The guidance algorithm was proven successful as it navigated an S-shaped path. As it encountered junctions, the robot was able to decide which branch of the maze to take.

Reversing after Front Bumper Activation
Of paramount importance was the robot's response to dead ends, where activation of its front bumper against a barrier prompted a precise 180 ° turn, retracing its path and selecting an alternative branch. Concurrently, it recorded the incorrect choice, facilitating a learning process. When the chosen path led to continued progress without encountering a dead end, the robot committed it to memory as the correct branch.

This iterative process persisted until the robot successfully reached the destination point in the maze. 

Finally, the project took our team around three weeks to complete and all related sources, files and references will be attached at the end of this report.

___________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________![IMG_5991](https://github.com/quangminhtra/EEBOT-MAZED-PROJECT_COE_538/assets/130938825/7105ae5a-a288-48f9-869e-961ecbed965b)


https://github.com/quangminhtra/EEBOT-MAZED-PROJECT_COE_538/assets/130938825/c0cb475a-b46d-40c4-80cf-9c7e72718ae4


Challenging tasks:

Deciding the eebot threshold sensors:

Determining the appropriate threshold values proved challenging during the execution of the maze-solving algorithm. The intricate process of  choosing values for darks and lights, essential for eebot's path determination, consumed significant testing time.

Resolution: The first step was to figure out the light and dark values for the eebot. This involved just placing the eebot on a dark surface and then on a light surface and reading out the values each time, for each sensor. For sensors A-D, figuring out the threshold values was easy  Since these sensors just had to recognize light from dark, a value reasonably lower than the dark values, read from the eebot when testing on a dark surface, were used. The EF sensors proved more challenging because only one value in memory was attributed to the difference between the two sensors, so as to not stray away from this defining property of the sensors. Boiled down, the process to find the threshold value was to cover each sensor with a finger, record the value and , once the whole process finished, take a value equidistant from the two recorded values. Of course, variance constants were added to the program as well in order to make up for any errors in the sensor readings.


Eebot does not determine the correct direction at the finish line:

Upon reaching the finish line, eebot failed to follow the proper procedure, turning left at the intersection as per the maze's design. Instead, it retraced its path back to the starting position.

Resolution: Due to the demonstrated shortage of time, we have yet to figure out how to correct it properly. Specifically, as per our prediction, the main problem may lie in how we set up the state that came to an error in how the eebot detects it.


Conclusion:
In conclusion, our collaborative efforts enabled Eebot to navigate through 90% of the maze successfully. This undertaking enhanced our understanding of assembly language and deepened our knowledge of utilizing light sensors to guide reboots on their path. Additionally, the project provided valuable opportunities for teamwork, enabling improved efficiency and an improved learning experience for all involved. We sincerely value the efforts invested in this project and the insights gained in the COE 538 course. We truly appreciated this experience, which contributed significantly to our understanding and application of relevant concepts.
