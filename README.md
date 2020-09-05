# Voice-Controlled-Dynamixel

The goal of the project was to utilize speech to make a dynamixel move. The user would speak into their computer's microphone and give a command such as “move” which would then trigger the dynamixel to move,  this would be a proof of concept that speech could be used to control robotics. In order for this to be done python and arduino had to be used. Python would be used to carry out the speech recognition aspect of the project due to the fact that it contained modules for speech to text recognition. While the Arduino IDE was responsible for controlling the dynamixel. In order to be able to be able to communicate effectively to each other, serial communication had to be used. With serial communication data gained through speech recognition could be sent to the arduino over the same port. Arduino would receive that data and send those commands to the dynamixels. The dynamixels would then receive those commands and move to the preset positions. 

In python speech recognition and serial communication both had to be set up. In order to properly identify the users voice and words, the speech recognition module, PyAudio module and the Google Speech API had to be used. The PyAudio module allows the user to access their microphone within the python code the computer's microphone is set up as the source(or input). The speech recognition module gave access to the recognizer class which made it possible to recognize speech.  Finally, the Google Speech API which is a machine learning API was used to convert speech to text.  In order to utilize serial communication with python we have to use the Pyserial module. This module sets up the port that python will be communicating through(ex. COM 8) and the baud rate (speed that bits of data will be sent). Along with this it allows for the usage of methods that are used to send and receive data through serial communication. 

The arduino’s function is to read data received through serial communication and use that data to control the dynamixels. In order to control the dynamixels (AX-12A) the Dynamixel Workbench library was utilized. This library initializes communication with the dynamixel and sends the dynamixel position commands. These position commands are activated if the data received through serial communication matches up with the expected value. The goal of the project is effectively achieved as the dynamixels respond to voice commands that are spoken to the computer. 
