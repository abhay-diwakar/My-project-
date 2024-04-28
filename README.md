# Automatic-room-light-control
An arduino based room light/fan control with Bidirectional visitor counter

# ABSTRACT
In this project, we will see the Automatic Room Lights using Arduino and PIR Sensor, where the lights in 
the room will automatically turn ON and OFF by detecting the presence of a human.
Such Automatic Room Lights can be implemented in your garages, staircases, bathrooms, etc. where we 
do not need continuous light but only when we are present.
Also, with the help of an automatic room light control system, you need not worry about electricity as 
the lights get automatically off when there is no person.
So, in this DIY project, we have implemented Automatic Room Lights using Arduino and PIR Sensor.

# INTRODUCTION
Intelligent Energy Saving System, the aim of the project is to save the energy. In this project we are using 
various sensors, controlling and display. However, in this project work the basic signal processing of 
various parameters which are temperature, LDR, Smoke sensor. For measuring various parameters 
values, various sensors are used and the output of these sensors are converted to control die 
parameters. The control circuit is designed using micro-controller. The outputs of all the three 
parameters are fed to micro controller. The output of the micro-controller is used to drive the LCD 
display, so that the value of each parameter can be displayed. In addition to the LCD display microcontroller outputs are also used to driver a relay independently. This relay energizes and de- energizes 
automatically according to the condition of the parameter.

# LITRRATURE SURVEY
Literature survey is the study of already established systems and collection of information which helps in 
doing new tasks. We propose a system which operates with control of relays and with the use of WAGO 
PLC (Programmable Logic Controller) and Arduino Uno. Switching operation of devices such as tube light, 
fan, AC, etc. can be operated spontaneously by using PIR sensor and on the basis of environmental 
conditions. In real-time implementation, automatic control is done by sensor data and manual control is 
done by android application.
But, difficulty in this paper is the controlling and monitoring of devices done by WAGO PLC and Arduino 
Uno both. These operations can be done by using only Arduino Uno. Maslekar et al proposed a smart 
lighting system in which Raspberry Pi has used. Raspberry Pi is monitoring lights and fans 
simultaneously. In the absence of person room lights and fans will automatically turns OFF. Energy is 
preserved by using this smart lighting system. The experimental results of this system have shown that 
50% energy is conserved. But the difficulty is Raspberry Pi is more expensive than Arduino Uno. 
Automatic Lighting and Control System for Classroom in which electrical light is controlled by Bluetooth, 
PIR sensor and relay. To switch ON or OFF the light Bluetooth module is connected to Arduino Uno which 
sends voice command from Arduino Uno by using the mobile android application. This paper can be implemented by removing the 
Bluetooth module as well. In the disquisitions speak about automatic room light system by using 
visitor counters operation. Depending upon the human presence, the room lights ON or OFF. There is no 
need of manual operation for switching. The PIR sensor is used to the human presence which is at the 
entrance of room. As visitor counter is used, there is increment in the counter when person enters in the 
room and this leads to turn ON the room light which is controlled by microcontroller program. If person 
exits the room, the counter decremented and this leads to tum OFF the lights. When all persons left the 
room then only lights in the room switched OFF. The difficulty in this system is that the door of room 
should not allow more than one person at a time. Arduino Ethernet shield and a wireless router device is used to built the network communication. The specific 
Android application is used to load the Modbus program into mobile or Windows software named 
"mypro" and on Arduino board, Arduino code loaded through USB (Universal Serial Bus) cable. There is 
interconnection between Arduino Ethernet Shield and mobile through Ethernet cable and router. By 
connecting to router, user can control and monitor the appliances easily.

# HARDWARE REQUIREMENT/DESCRIPTION
The list of necessary components items required are mentioned below:
Components Details

Solderless Breadboard, 
Arduino Uno,
ultrasonic sensor hc-sr04 ×2,
16×2 LCD Display,
100R Resistor,
4.7k Resistor,
1k Resistor,
1-Channel 5v Relay Module,
Male to Male Jumper Wires,
Male to Female jumper Wires,
220v LED Bulb, holder,
5v 2Amp Power Adapter,
Plug with wires attached,
Small wires for breadboard and long wires

# Software Used
Software used to control this system is Arduino IDE (Integrated Development Environment). This 
software is used to write the program and compile it to the Arduino Uno board. Therefore, the arduino 
software commands control the arduino board, sensing devices and another circuitry.

# WORKING OF THE SYSTEM
The project of “Digital visitor counter” is based on the interfacing of some components such as sensors, 
motors etc. with arduino microcontroller. This counter can count people in both directions. This circuit 
can be used to count the number of persons entering a hall/mall/home/office in the entrance gate and it 
can count the number of persons leaving the hall by decrementing the count at same gate or exit gate 
and it depends upon sensor placement in mall/hall. It can also be used at gates of parking areas and 
other public places.
This project is divided in four parts: sensors, controller, counter display and gate. The sensor would 
observe an interruption and provide an input to the controller which would run the counter increment 
or decrement depending on entering or exiting of the person. And counting is displayed on a 16x2 LCD 
through the controller.
When any one enters in the room, Ultrasonic sensor will get interrupted by the object then other sensor 
will not work because we have added a delay for a while.

![11](https://user-images.githubusercontent.com/74290353/221350288-d05aabe0-4726-4ed1-8d6d-b4b41707e8c6.png)

# CIRCUIT EXPLANATION
There are some sections of whole visitor counter circuit that are sensor section, control section, display 
section and driver section.
Sensor section: In this section we have used two Ultrasonic sensor modules which contain Ultrasonic
diodes, Arduino, and LED’s. Potentiometer is used for setting reference voltage at comparator’s one 
terminal and Ultrasonic sensors sense the object or person and provide a change in voltage at 
comparator’s second terminal. Then comparator compares both voltages and generates a digital signal 
at output. Here in this circuit we have used two comparators for two sensors. Arduino is used as 
comparator. Arduino has inbuilt two low noise Op-amp.
Control Section: Arduino UNO is used for controlling whole the process of this visitor counter project. 
The outputs of comparators are connected to digital pin number 14 and 19 of arduino. Arduino read 
these signals and send commands to relay driver circuit to drive the relay for light bulb controlling. If you 
find any difficulty in working with relay, check out this tutorial on arduino relay control to learn more 
about operating relay with Arduino.
Arduino Uno As Processing Unit: Arduino Uno is a microcontroller in which ATmega328 microprocessor 
is used which is shown in the Figure 2.
It has 6 analog input pins and 14 digital input or output pins which can be used as PWM(Pulse Width 
Modulation) outputs. It has its own programming language. The crystal oscillator frequency of this 
microcontroller is 16MHz. It has USB cable which can simply connect with computer, power barrel jack, 
reset button and ICSP (In Circuit Serial Programming). Each pin of the Arduino Uno is operated at 5V.The 
programming language of this microcontroller is not complex.
Display section: Display section contains a 16x2 LCD. This section will display the counted number of 
people and light status when no one will in the room.
Relay Driver section: Relay driver section consist a BC547 transistor and a 5 volt relay for controlling the 
light bulb. Transistor is used to drive the relay because arduino does not supply enough voltage and 
current to drive relay. So we added a relay driver circuit to get enough voltage and current for relay. 
Arduino sends commands to this relay driver transistor and then light bulb will turn on/off accordingly.
A relay is a digital switch that controls much higher currents and voltages. This device is widely used in 
power protection. The benefits of this device are small in size, stability and long-time reliable and it can 
be also used for both ac and dc systems. Relay has three terminals that are normally closed terminal, 
normally open terminal and common terminal. It has three pins GND, VCC and input signal.

# Visitor Counter Circuit Diagram
The outputs of IR Sensor Modules are directly connected to arduino digital pin number 14(A0) and 
19(A5). And Relay driver transistor at digital pin 2. LCD is connected in 4 bit mode. RS and EN pin of LCD 
is directly connected at 13 and 12. Data pin of LCD D4-D7 is also directly connected to arduino at D11-D8 
respectively. Rest of connections are shown in the below circuit diagram.

![22](https://user-images.githubusercontent.com/74290353/221350285-f96e1c28-39de-478d-b6c3-59357e5ace2c.png)

# CONCLUSION
The paper has introduced the idea of automated homes and proposed a method which saves power 
consumption by system. This Automated Gadget Control System having the interconnections between 
the home appliances and sensors for contrelling and monitoring the device. Automated home is a vast 
system that having multiple technologies and its applications that can be used to provide control and 
security of the homes easily.

# FUTURE WORK
There are many technologies that can be used in automatic lighting systems to make the system more 
accurate. To make the system more professional GSM (Global System for Mobile) module can be used to 
get notifications. There are some sensors that can be used to control and secure the home. For example, 
pressure sensor used to detect the occupancy which will be placed outside the door. Image processing 
can also be used to detect a person's presence by using digital camera.

# REFERENCES
1) Vibhuti and Shimi S.L., "Implementation of Smart Class Room Using WAGO PLC", Proceedings of the 
Second International Conference on Inventive Systems and Control (ICISC) 2018, Coimbatore, pp. 807-812.
2) A. Maslekar, K. Apama, K. Mamatha and T.Shivakumara, "Smart Lighting System using Raspberry Pi", 
International Journal of Innovative Research in Science and Technology, Vol.4(7), 2015, pp.5113-51211.
3) Suresh S, H.N.S.Anusha, T.Rajath, P.Soundarya and S.V,PrathyushaVudatha. "Automatic Lighting And 
Control System For Classroom" 2016 International Conference on ICT in Business Industry & Goverment 
(ICTBIG).
4) Vahid Hassanpour, Sedighe Rajabi, Zeinab Shayan, Zahra Hafezi, Mohammad Mehdi Arefi, "Low-Cost 
Home Automation Using Arduino and Modbus Protocol", 5th International Conference on Control, 
Instrumentation and Automation (ICCIA), Shiraz, 2017, pp. 284-289.
5) https://components101.com/microcontrollers/arduino-Uno

# TinkerCad Simulation

![33](https://user-images.githubusercontent.com/74290353/221350291-a5cc7a6e-30d0-44eb-aada-f1fbb0036403.png)

# Finished Model Image

![55](https://user-images.githubusercontent.com/74290353/221350536-66cce41c-7895-4fdf-85e6-5f3b16577e9c.png)
