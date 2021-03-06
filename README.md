# Capstone Project - The Factory Rover
![slow good 2019-05-02 21_26_50](https://user-images.githubusercontent.com/46872807/57117360-0bc02180-6d21-11e9-8744-bf53d3017b89.gif)

<img width="578" alt="Best lable" src="https://user-images.githubusercontent.com/46872807/57146020-021ed400-6d8a-11e9-96c7-daa7ff4aac60.png">

Video of the Rover in action https://www.youtube.com/watch?v=8NFM5vZpSac

The Factory Rover was developed as my senior capstone project in high school. My group decided to address efficiency in factories through an omnidirectional rover. The Factory Rover was intended to solve this issue by providing an automatic mapping system and by allowing remote control of the rover to move packages and materials. Though these goals were not achieved in to their highest expectations, we ended up with a unique project that met the majority of our goals. Our project is capable of reading handwritten digits and moving in different directions based on these digits and is capable of being controlled manually over WIFI. Our Rover can move in all directions because of the use of mecanum wheels in its design.
## Arduino Control
The Arduino acts as the master controller of inputs and outputs within the system. This means that the Arduino communicates with the Raspberry Pi via serial, receives digital inputs from the on-board switches/button, and controls the LCD display and motors. With all these inputs, the Arduino is constantly checking for conditions to be met and running if loops. Once conditions are met, the Arduino updates the LCD display and runs motors accordingly.
## Raspberry Pi 
The Raspberry Pi controls the more advanced computing of the Factory Rover. The Raspberry Pi waits for the mode of the Factory Rover to be sent to it via its serial connection to the Arduinio. After receiving the mode, the Raspberry Pi either acts as a WIFI receiver which relays data to the Arduino, or takes an image with its camera and runs a Neural Network, outputting the value of the network to the Arduino. 
## Neural Network
To develop the Neural Network, many new skills were acquired. I had to learn the syntax of Python, understand a good amount of the data science and linear algebra that neural networks are based in, and understand how Numpy and the TensorFlow libraries utilize data science and linear algebra. The Neural Network that the Rover uses has 3 hidden layers and uses multiple activation functions. The Network was trained with the MNIST data set and ultimately achieved a 94% accuracy in testing. On the Rover, the Neural Network interprets digits and is key to the longevity of the project.
