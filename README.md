```
CYPRUS INTERNATIONAL UNIVERSITY
FACULTY OF ENGINEERING
```
DEPARTMENT OF ELECTRICAL & ELECTRONICS ENGINEERING

```
DEPARTMENT OF COMPUTER ENGINEERING
DEPARTMENT OF MECHATRONICS ENGINEERING
```
```
IMPLIMENTATION OF FIRST-PERSON VIEW (FPV)
RACING DRONE USING ARDUINO
```
```
By
Ali DOGAN (CMPE)
Laure KAMWENYI (EELE)
Mujtaba ABDALLA (CMPE)
Mohamed IBRAHIM (MCTE)
Muhammad MUAWAZ (MCTE)
```
```
February, 2023
Nicosia, NORTH CYPRUS
```

```
CYPRUS INTERNATIONAL UNIVERSITY
FACULTY OF ENGINEERING
```
**DEPARTMENT OF ELECTRICAL & ELECTRONICS ENGINEERING**

```
DEPARTMENT COMPUTER ENGINEERING
DEPARTMENT OF MECHATRONICS ENGINEERING
```
```
IMPLIMENTATION OF FIRST-PERSON VIEW (FPV)
RACING DRONE USING ARDUINO
```
```
By
Ali DOGAN (CMPE)
Laure KAMWENYI (EELE)
Mujtaba ABDALLA (CMPE)
Mohamed IBRAHIM (MCTE)
Muhammad MUAWAZ (MCTE)
```
```
February, 2023
Nicosia, NORTH CYPRUS
```

```
IMPLIMENTATION OF FIRST-PERSON VIEW (FPV)
RACING DRONE USING ARDUINO
```
```
By
Ali DOGAN
Laure KAMWENYI
Mujtaba ABDALLA
Mohamed IBRAHIM
Muhammad MUAWAZ
```
DATE OF APPROVAL:

APPROVED BY:

Asst. Prof. Dr. Öykü AKAYDIN


```
iii
```
**ABSTRACT**
First-person view (FPV) racing drones are unmanned aerial vehicles (UAVs) designed
for high-speed racing and acrobatic flight. They have become a popular hobby and competitive
sport worldwide due to the thrill of piloting a drone in real-time, using a first-person view from
the drone's perspective.

FPV racing drones are built with lightweight materials and equipped with powerful
motors, high-speed controllers, and lightweight cameras that transmit live video feed to the
pilot on the ground. The drones are flown using remote control units that mimic the motion and
orientation of the drone. The pilot sees the drone's view through a headset or a screen that
displays the video feed. Racing drones are designed to be highly manoeuvrable and capable of
reaching high speeds, making FPV racing a challenging and adrenaline-fueled sport. Pilots race
through obstacle courses, performing acrobatic stunts, and competing to achieve the fastest lap
times. The popularity of FPV racing has led to the formation of organized leagues and
competitions, with races held worldwide, including the World Drone Racing Championships.

Building a first-person view (FPV) drone using Arduino components is an exciting and
challenging project that combines coding, electronics, and mechanics. An FPV drone allows
users to fly and control a small quadcopter equipped with a camera that streams live video to a
video display, providing a unique aerial view. To build an FPV drone using Arduino
components, one needs to select and assemble various components such as the flight controller,
motors, propellers, battery, and camera, and then program the Arduino board to control the
drone's movements and camera. This project requires a basic understanding of electronics and
programming, and it offers a rewarding experience to learn and apply these skills in a fun and
innovative way.

In conclusion, first-person view racing drones are a rapidly growing hobby and
competitive sport that provides a unique and thrilling experience for pilots. While they present
some safety and legal challenges, advances in technology and regulations are helping to ensure
that the sport continues to grow and evolve while ensuring the safety of participants and the
public.


```
iv
```
**ÖZET**


## v

**TABLE OF CONTENTS**

ABSTRACT ................................................................................................................ iii




viii

- CHAPTER ONE – INTRODUCTION ÖZET iv
- 1.1 Purpose of this Project
- 1.2 Project Description..................................................................................................
- 1. 3 Justification of Proposed System
- 1. 4 Overall System Functionality
- CHAPTER TWO – EXISTING SYSTEMS AND TECHNOLOGIES
- 2.1 3 - D Printed Drone
- 2.1.1 Project Description............................................................................................
- 2.1. 2 Comparison of projects
- 2.2 Drone for Civil Applications
- 2.2.1 Project Description............................................................................................
- 2.2. 2 Comparison of projects
- 2. 3 YMFC-AL Self-Levelling Arduino Drone
- 2. 3 .1 Hardware used in mentioned project
- 2. 3 .2 Circuit Diagram
- CHAPTER THREE – REALISTIC CONSTRAINTS
- 3 .1 Design Constraints
- 3 2 Engineering Standards and Lifelong Learning
- 3 .3 Economical Analysis
- 3 .4 Sustainability.........................................................................................................
- 3.5 Ethics Issues
- 3.6 Health and Safety Problems vi
- 3.7 Social and Political Issues
- 3. 8 Environmental Impact
- 3. 9 Manufacturability
- 3. 10 Risk management, and Change management
- 3. 11 Legal Consequences............................................................................................
- CHAPTER FOUR – SYSTEM DESIGN
- 4 1 System Structure
- 4 2 Components Used and Their Description
- 4. 2 .1 Frame
- 4. 2 .2 Brushless Motors, Electronic Speed Controllers, and Propellers
- 4. 2 .3 3S LiPo Battery
- 4. 2 .4 Arduino Uno R3
- 4. 2 .5 Mini Breadboard
- 4. 2 .6 Gyroscope/Accelerometer MPU
- 4. 2 7 FlySky Controller and Receiver......................................................................
- 4. 2 .8 ESP32-CAM (Camera) with USB to TTL Converter
- 4. 2 9 ESP32-WROOM-32U
- 4. 2 10 GY-NEO6MV2 GPS Module
- 4 3 System Circuits
- 4. 3 .1 Quadcopter Circuit
- 4. 3 .2 ESP32-CAM Circuit
- 4. 3 .3 GY-NEO6MV2 GPS Module and ESP32-WROOM- 32 U Circuit
- 4 4 How the System Works
- CHAPTER FIVE – CODE CONCEEPT vii
- 5 .1 Drone Programming..............................................................................................
- 5 .1.1 Calibration of Controller, Receiver, and Gyroscope
- 5 .1.2 Calibration of ESCs and Controller, Gyroscope, and Motor Testing
- 5.1. 3 Flight Controller Code
- 5 2 Method of Calculation
- 5. 2 .1 Calibration.......................................................................................................
- 5. 2 .1.1 Calculating the Position of the Control Sticks
- 5.1.1. 2 Gyroscope Axis Calibration
- 5. 2 .2 Calibration of ESCs and Controller, and Gyroscope Testing
- 5. 2 .2.1 Controller Testing and ESC Throttle Calibration
- 5.2.2.2 Gyroscope/Accelerometer Testing
- 5.2.2.3 Motor Testing and Propeller Balancing
- 5.2.3 Flight Controller..............................................................................................
- 5.2. 3 .1 Controller
- 5.2. 3 .2 Modifying Motor Speed in Case of Voltage Drop....................................
- 5 3 Camera, GPS, and Wi-Fi Module Code Concept
- 5. 3 .1 Camera Program and Display
- 5. 3 2 GPS and Wi-Fi Program
- CONCLUSION
- APPENDICIES
- REFRENCES
- Figure 1.1: Overall System Functionality LIST OF FIGURES
- Figure 2.1: Drone for Civil Applications
- Figure 2.2: YMFC-AL Self-levelling Drone Circuit Diagram
- Figure 4.1: Block Diagram
- Figure 4. 2 : DJI F450
- Figure 4. 3 : Brushless Motors, ESCs, and Propellers
- Figure 4. 4 : 3S LiPo Battery
- Figure 4. 5 : Arduino Uno R3
- Figure 4. 6 : Mini Breadboard..................................................................................
- Figure 4. 7 : Gyroscope/Accelerometer MPU
- Figure 4. 8 : FlySky Controller and Receiver RC
- Figure 4. 9 : ESP32-CAM and USB to TTL Converter
- Figure 4. 10 : ESP32-WROOM-32U Wi-Fi and Bluetooth Module
- Figure 4.1 1 : GY-NEO6MV2 GPS Module
- Figure 4.1 2 : Quadcopter Circuit Diagram
- Figure 4.1 3 : ESP32-CAM connected to a USB to TTL Converter
- Figure 4.1 4 : GPS and Wi-Fi Module Circuit


```
ix
```
**LIST OF TABLES**

Table 3.1: List of Components Used and their Prices ........................................... 11


```
CHAPTER ONE
INTRODUCTION
```
Drone inclusion into the entertainment industry is just as expansive and inventive as the
entertainment industry itself. First-person view (FPV) drones may be fairly expensive to buy
or construct, therefore this project wants to support the expanding industry and create a
personal, inexpensive FPV drone in the hopes of igniting innovation and advancement in this
vast and enjoyable sector.

By employing drones in the entertainment sector, aerial photography and videography
are now more accessible to filmmakers, photographers, and videographers. Drone flight now
includes an immersive and interactive experience with the integration of FPV technology. The
creation of an affordable FPV drone can open up this technology to a wider group of
enthusiasts, amateurs, and professionals in response to the rising demand for video captured by
drones. In addition to making flying more enjoyable for everyone, this project intends to
promote creativity and breakthroughs in the industry. The outcome will be a drone that is not
only simple to operate but also offers an enjoyable and high-quality flying experience.

The demand for FPV racing drones has increased alongside the inventive uses in the
entertainment sector. Pilots in FPV drone racing compete against one another while flying their
drones at fast speeds and navigating through obstacle courses. This rapidly expanding industry
of FPV racers is constantly searching for updated gear that will offer them an advantage on the
track. This project intends to serve this community and spread the thrill of racing to a larger
audience by creating a personal and cheap FPV racing drone. The objective is to create a drone
that can be operated by both inexperienced and seasoned pilots, with an emphasis on high
performance, agility, and durability.


**1.1 Purpose of this Study**

The purpose of this study is to provide comprehensive information on the steps involved,
budget, factors taken into account, and potential challenges during the course of this project.
This study also evaluates and contrasts other comparable projects to ensure the project can
stand out as a cost-effective and reliable option. It is imperative to address the legal implications
of a project in order to avoid any legal issues in the future, which is why this report covers that
aspect as well.

## 1.2 Project Description..................................................................................................

This project proposes the development of a First-Person View (FPV) racing drone. An
FPV drone is a remotely controlled aerial vehicle equipped with a camera, allowing the user to
control the drone by viewing the live footage either on a screen display or through special
goggles with an integrated display.

The design of this FPV drone is intended to be much simpler compared to other FPV
drones in the market. The central component of the drone, the microcontroller, serves as its
brain, controlling aspects such as the speed of the propellers and motion. To enhance its speed
and manoeuvrability, the primary frame of the drone will be constructed from lightweight
carbon fibre, keeping it as small as possible.

The microcontroller, batteries, power distributor, and dc brushless motors (propellers)
will be connected to the video transmitter from the camera, with a receiver receiving the video
signals and transmitting it to either a display screen or FPV goggles.

Moreover, this project will take into consideration the safety aspect and regulations set
by the relevant authorities. The FPV racing drone will be designed to meet the safety standards
and regulations in order to ensure the safety of the user and those around the drone during
operation. Additionally, the project will incorporate the latest technology available, making it
user-friendly and efficient in operation. This will contribute to the growing popularity of FPV
racing and provide a platform for enthusiasts to engage in the sport safely and effectively.


## 1. 3 Justification of Proposed System

The FPV drone market is characterized by the high cost of drones and their complex
construction and programming. However, this project aims to provide an affordable, reliable
and user-friendly alternative to the existing drones in the market. This will be achieved through
the use of lightweight components and a simplified approach to programming, making it easier
to both manufacture and operate.

Furthermore, the affordability of this FPV drone project is not at the cost of quality. The
use of modern technology and innovative design will ensure that the drone performs optimally
and meets the standards set by the relevant authorities. This project will provide an accessible
entry point for those interested in the FPV racing industry, fostering growth and creativity
within the field.

## 1. 4 Overall System Functionality

The microcontroller acts as the central processing unit of the drone and is programmed
to control various functions, including motion control, propeller speed, video transmission, and
power distribution. To ensure seamless video transmission, the receiver will be matched with
the frequency of the transmitter, enabling the video signals to be displayed on either the screen
or the FPV goggles. Figure 1.1 shows how the system functions overall.


```
Figure 1.1: Overall System Functionality.
`
```
```
Microcontroller
```
motor

```
motor
```
```
motor
```
```
motor
```
```
camera
```
```
Video
transmitter
```
```
Video Receiver
```
```
Video display
```
```
Controller Control^
transmitter
```
```
Control
Receiver
```

**CHAPTER TWO**

EXISTING SYSTEMS AND TECHNOLOGIES

**2.1 3D Printed Drone**

A team from the Mechanical Engineering Department at Prince Mohammed Bin Fahad
University created this project as part of a senior design project^ [1].

## 2.1.1 Project Description............................................................................................

The objective of this project is to design a quadcopter and conduct research to enhance
its performance through experimentation and testing to achieve the optimal outcome. The team
has analysed various factors such as flight stability, power efficiency, and manoeuvrability to
identify areas for improvement. Based on the findings, modifications have been made to the
design, and the quadcopter has been tested again to assess the impact of the changes. The
process has been repeated until the desired results are achieved.

## 2.1. 2 Comparison of projects

A- The 3D printed drone project incurred a cost of $1902.58 due to multiple 3D-printing
of drone parts for modifications and rebuilding. However, this will not be the case in our project
as we plan to purchase a ready-to-use drone frame, which will reduce the total cost. The cost
of 3D-printing alone in the previous project was $1332.62.

B- This project utilized a flight controller for the 3D Printed Drone, but we plan to use
an Arduino-Uno for our project and program all the operations.

C- The aim of the 3D Printed Drone project was to research and find solutions to
maximize flight time while minimizing cost. Conversely, our project aims to create a high-
speed, lightweight drone with the ability to manoeuvre quickly.


## 2.2 Drone for Civil Applications

This project was done by a team from the Department of Electrical and Electronic
Engineering at Brac University^ [2].

## 2.2.1 Project Description............................................................................................

The purpose of this project is to create a drone that is capable of serving multiple
functions, such as surveillance and delivery of light-weight products. The aim is to design a
drone that is efficient and practical for these specific uses. Additionally, the team has considered
various factors such as flight stability, durability, and payload capacity during the design
process to ensure that the drone meets the desired performance requirements.

```
Figure 2.1: Drone for Civil Applications
```
## 2.2. 2 Comparison of projects

A- The drone for civil applications project's goal was to deliver light-weight products,
which is not the focus of our project as it is not designed for lifting objects.

B- While this project aimed to use the drone for various surveillance purposes, this is not
a primary objective in our project, although it can still be used for such purposes.

C- This project utilized an Android Application to track the drone's location, which will
not be used in our project.


## 2. 3 YMFC-AL Self-Levelling Arduino Drone

The YMFC-AL is an Arduino based self-levelling drone that uses a gyroscope equipped
with an accelerometer to level itself once the controls are released^ [3]. This project will be the
main guideline as it is a based level drone using almost the same equipment the project at hand
uses to build the FPV drone.

2.3.1 Hardware Components Used in the Project

- 1 x 450 size frame with integrated power distribution board
- 4 x 1000kV motor / 10x4.5 props / ESC combo
- 1 x 3S / 2200mAh / 20C LiPo
- 1 x Arduino Uno
- 1 x MPU-6050 gyro / accelerometer
- 1 x FlySky FS-i6 6-CH TX Transmitter
- 1 x 2S/3S LiPo battery charger


## 2. 3 .2 Circuit Diagram

Figure 2.2 shows this project’s circuit diagram. The control receiver, and the MPU 6050
gyroscope are directly connected as inputs to the Arduino which will process the information
both components will input as the Arduino is the flight controller of the drone. The power
connections of the ESCs are connected through the frame along with the battery as the frame
is used as an electric conductor. The information pins of the ESCs are connected to the Arduino
as output. The motors are connected to the ESCs as the ESCs control how much power is given
to each motor.

```
Figure 2.2: YMFC-AL Self-levelling Drone Circuit Diagram
```

```
CHAPTER THREE
REALISTIC CONSTRAINTS
```
## 3 .1 Design Constraints

Design constraints for FPV racing drones are crucial to consider as they have a direct
impact on the drone's performance and capabilities. Some key constraints include weight and
size, as racing drones need to be lightweight and compact to achieve high speeds and agility.
The power system must also be optimized for maximum efficiency, which includes the motor,
battery, and electronic speed controller. Additionally, the design must include a durable frame
that can withstand the stress of high-speed flying and collisions, while also providing easy
access to internal components for maintenance and repair. Another important constraint is the
drone's aerodynamics, which must be designed for stability and manoeuvrability. Finally, the
choice of materials and components used in the drone must also meet regulatory requirements
for safe operation, such as radio frequency compatibility and fire safety standards.

Another important factor in the design of FPV racing drones is the combination of the
onboard camera and video transmission system. The camera must not only capture high-quality,
real-time video, but it must also be small and lightweight to not affect the drone's performance.
The video transmission system must provide a clear video to the pilot through a robust and
stable connection, while also complying with legal frequency bands and power limits. The
integration of these systems with the rest of the drone's components must be thoroughly
planned to ensure the best performance and ease of use. Additionally, the design of the control
system is vital as it must enable the pilot to control the drone with precision and ease, even in
challenging flying conditions. Ultimately, designing an FPV racing drone requires a careful
balancing of various constraints to achieve the desired performance and capabilities.

## 3 2 Engineering Standards and Lifelong Learning

Engineering standards and continuous learning are essential components in the FPV
racing drone industry. Engineers must stay informed of the current industry standards,
regulations, and best practices to design and build safe drones that meet necessary
requirements. Keeping up with professional development and the latest advancements in the
field is crucial to their success. As the FPV racing drone industry is constantly evolving,
engineers must be willing to continuously expand their knowledge by learning new


technologies, techniques, and design methods. This requires a flexible mindset and an openness
to new challenges to keep up with the latest trends and innovations. By committing to lifelong
learning and adhering to strict engineering standards, engineers in the FPV racing drone field
can guarantee the reliability and quality of their work, driving the growth and development of
this exciting industry.

## 3 .3 Economical Analysis

Table 3.1 is a list compiled of the parts used along with their prices (it is to be mentioned
that due to the country’s political conditions the prices would normally be a lot less than
mentioned in table 3.1)

```
Table 3.1: List of Components and their Prices
Component Quantity Price ($)
Frame (DJI F450) 1 30
Brushless motors + ESCs +
propellers
```
```
4 each 120
```
```
3s LiPo Battery 11.4V 1 42.
Arduino Uno R3 1 28
MPU 6050
Gyroscope/Accelerometer
```
### 1 5

```
FlySky Controller and
Receiver
```
### 1 130

```
ESP32-CAM (Camera) +
USB to TTL converter
```
### 1 31

### ESP32-WROOM-32U

```
(Wi-Fi/Bluetooth module)
```
### 1 4

### GY-NEO6MV

```
GPS module
```
### 1 44

```
Mini Breadboard 1 5
Jumping wire kit 1 7
Total ($) 447
```

## 3 .4 Sustainability.........................................................................................................

The significance of sustainability in the creation and manufacturing of consumer
products, including FPV racing drones, is growing. A relevant factor of sustainability when it
comes to these drones is the composition of materials used in their construction. A considerable
amount of racing drones are constructed from non-biodegradable plastic and petroleum-based
materials, which can harm the environment when discarded. To combat this, some producers
are opting for environmentally friendly materials, like biodegradable plastics and bamboo,
which have a reduced impact on the planet.

Another aspect of sustainability that is relevant to FPV racing drones is the energy used
during their operation. Racing drones require a lot of power to fly and are often powered by
lithium-polymer batteries that are not easily recyclable. To address this issue, some
manufacturers are exploring alternative power sources, such as hydrogen fuel cells, which have
a lower environmental impact. Additionally, some manufacturers are developing more energy-
efficient drones that use less power during flight, which can help to reduce their carbon
footprint. By incorporating sustainable design principles into the production of FPV racing
drones, manufacturers can help to create a more environmentally-friendly future for this rapidly
growing sport.

## 3.5 Ethics Issues

There are several ethical issues that can arise in an FPV racing drone project. One concern
is privacy and surveillance, as drones equipped with cameras can potentially record images and
videos of individuals without their consent. This raises questions about the responsible use of
drone technology and the need for privacy laws to be updated to address these new concerns.
Additionally, the use of drones in crowded public spaces can also raise safety concerns, as the
fast-moving and sometimes unpredictable nature of drones can pose a threat to other people.
It's crucial for the drone community to abide by ethical principles and consider the impact of
their drone projects on others. Furthermore, the responsible disposal of drone batteries and
other electronic waste is another ethical concern, as they contain harmful substances that can
pose a risk to the environment and wildlife. Ensuring that the production, use, and disposal of
FPV racing drones align with ethical principles is crucial to promote sustainable and
responsible technology practices.


**3.6 Health and Safety Problems**

FPV racing drones have become increasingly popular in recent years, but there are
significant health and safety concerns associated with their use. One major concern is the
potential for collisions with other objects, such as buildings, trees, and other drones. The high
speeds at which these drones can travel, combined with their small size, make them difficult to
see and track, increasing the risk of accidents. In addition, the use of FPV racing drones requires
a certain level of manual dexterity, hand-eye coordination, and cognitive skills, which can be
negatively impacted by factors such as fatigue, stress, and alcohol consumption.

Another serious health and safety concern with FPV racing drones is their potential to
cause physical harm to individuals in close proximity to their flight path. The fast-moving
propellers and small size of these drones can pose a significant threat to people and animals,
particularly if they are flown in populated areas or near other people. Moreover, the high-
powered lithium-ion batteries used in these drones can pose a fire hazard if they are damaged
or overheated, increasing the risk of injury to both the drone operator and bystanders.
Additionally, the electromagnetic radiation emitted by these drones can pose a health risk to
those who are exposed to it, particularly if they are in close proximity to the drone for an
extended period of time.

## 3.7 Social and Political Issues

FPV racing drones have also raised several social and political issues. One of the main
concerns is privacy, as drones equipped with cameras can easily capture images and video
footage of individuals without their consent. This has led to concerns about the potential for
drones to be used for surveillance or to invade personal privacy. In addition, the use of drones
in urban areas has raised concerns about air traffic control, particularly in areas with high levels
of air traffic. There have also been concerns about the potential for drones to interfere with
other forms of air travel, such as commercial airliners and emergency services. Furthermore,
the increasing popularity of FPV racing drones has led to a growing demand for regulated
airspace, which has raised questions about the allocation of public resources and the balance
between safety and personal freedom.


FPV racing drones could be used unlawfully, which is another social and political
problem. Drones can be easily modified to carry dangerous payloads, such as weapons or
explosives, which poses a significant threat to public safety. In addition, drones can be used to
disrupt public events, transport illegal goods, and engage in other criminal activities, making it
difficult for law enforcement to regulate and control their use. Moreover, the lack of clear
regulations and guidelines regarding the use of drones has resulted in confusion and
inconsistent enforcement of laws, making it difficult to hold operators accountable for their
actions. The growing popularity of FPV racing drones has also raised concerns about the
allocation of public resources, including funds and manpower, to regulate and enforce laws
related to drone use. The need to address these social and political issues highlights the
importance of developing clear and comprehensive regulations and guidelines to ensure the
safe and responsible use of FPV racing drones.

## 3. 8 Environmental Impact

The environmental impact of FPV racing drones is a growing concern. The production,
use, and disposal of drones can have a negative impact on the environment. The manufacturing
process of drones requires a significant amount of energy and resources and can result in the
emission of greenhouse gases and other pollutants. In addition, the use of drones requires
batteries, which can contain hazardous materials and have a limited lifespan, leading to e-waste
and potential harm to the environment when disposed of improperly. Furthermore, the use of
drones in sensitive environments, such as wilderness areas and protected parks, can result in
soil erosion, vegetation damage, and other ecological impacts.

Additionally, the use of drones can result in direct harm to wildlife and their habitats.
FPV racing drones can cause disturbance to animals, leading to changes in their behaviour and
potential harm to individual animals and their habitats. The noise and presence of drones can
also disrupt migration patterns, mating behaviours, and nesting activities of wildlife, potentially
leading to population declines. Furthermore, drones can also interfere with scientific studies,
such as those aimed at monitoring and conserving endangered species, by disrupting their
normal behaviours and migration patterns. These environmental impacts highlight the
importance of responsible drone use and the need for regulations that balance the benefits of
FPV racing drones with the protection of wildlife, ecosystems, and the environment.


## 3. 9 Manufacturability

FPV racing drones have gained popularity in recent years, and their manufacturability
has greatly improved. With advances in technology, components such as motors, flight
controllers, and cameras are now more readily available and accessible to drone manufacturers.
Many of these components are designed specifically for FPV racing and offer reliable
performance at an affordable cost. This has made it easier for manufacturers to produce high-
quality, high-performance FPV racing drones that are readily available to consumers.
Additionally, the rise of 3D printing technology has allowed manufacturers to easily produce
custom drone parts, further streamlining the production process. Overall, the manufacturability
of FPV racing drones has greatly improved, making it easier for manufacturers to produce high-
quality drones that are accessible to a wide range of consumers.

**3.10 Risk Management and Change Management**

Risk management is a critical aspect when it comes to flying an FPV drone. This type of
drone is operated remotely and at high speeds, which can pose potential dangers to both the
drone operator and those nearby. To minimize these risks, it's important to follow all safety
guidelines and regulations set by the relevant authorities, such as the FAA in the US. Drone
operators should also ensure that their equipment is well-maintained and in good working
condition before each flight. In addition, it's important to fly in safe and appropriate areas, such
as open fields or designated flying zones, and avoid crowded or restricted areas such as airports
and urban areas. Operators should also familiarize themselves with the capabilities and
limitations of their drone and be mindful of weather conditions, such as strong winds or heavy
rain, that can impact its performance.

When it comes to FPV drones, change management is essential because the market is
always being introduced to new technology and regulations. Drone operators need to be able
to adapt to these changes and incorporate them into their operations. This may involve updating
their equipment, training themselves on new regulations and guidelines, or modifying their
flying practices to align with new requirements. In some cases, drone operators may need to
invest in new equipment or software to ensure compliance with new regulations. It's also
important to keep up-to-date with industry developments and stay informed about new products
and services that may improve the performance and safety of their FPV drones.


By effectively managing change, drone operators can ensure they are operating their
equipment in the most efficient and effective way, while also minimizing risks and maximizing
their enjoyment of the hobby.

## 3. 11 Legal Consequences............................................................................................

The legal consequences of FPV racing drones can vary greatly depending on the
jurisdiction and specific circumstances of the operation. In many countries, there are specific
regulations and guidelines that must be followed when flying drones, including FPV racing
drones. For example, the Federal Aviation Administration (FAA) in the US has established
guidelines for flying drones, including restrictions on altitude, flight paths, and flight
overpopulated areas. Drone operators who violate these regulations can face fines, legal
penalties, and even criminal charges.

In addition to regulations set by aviation authorities, there are also privacy and liability
concerns that must be taken into consideration when flying FPV racing drones. For example,
if a drone operates in a restricted or sensitive area, such as near an airport or a military base, it
may pose a risk to national security and result in criminal charges. Similarly, if a drone causes
injury or damage to property, the operator may be held liable for any resulting damages. It is
important for FPV drone operators to be aware of the laws and regulations surrounding drone
use and to follow them carefully to avoid legal consequences. Seeking legal advice before
operating an FPV racing drone is always advisable, as this can help to ensure compliance and
minimize potential risks.


```
CHAPTER FOUR
SYSTEM DESIGN
```
## 4 1 System Structure

Figure 4.1 shows the block diagram of the system. As the figure shows, the Arduino is
the centre of the drone, having the ESCs connected to it and the motors connected to the ESCs.
The controller receiver is also connected to the Arduino for movement. The camera and GPS
modules are connected to power from the Arduino via the mini breadboard. The Camera
broadcasts the video footage to the display which could be a laptop or a mobile phone.

```
Figure 4.1: Block Diagram
```
```
Arduino
```
### ESC

Motor (^) Motor

### ESC

```
Controller
```
```
Receiver
```
### ESC

```
Motor
```
### ESC

```
Motor
```
```
Camera,
GPS
```
```
Display
```

**4. 2 System Components**

```
This section will list the components used along with their description.
```
## 4. 2 .1 Frame

Figure 4.2 shows the frame used is the DJI F450 quadcopter frame. The reason this frame
was used due to the components not being compact enough for a smaller frame to be used
which could affect the speed of the quadcopter itself.

```
Figure 4. 2 : DJI F450
```

## 4. 2 .2 Brushless Motors, Electronic Speed Controllers, and Propellers

4 A2212 Brushless motors were used. They operate at 1400 RPM. The electronic speed
controllers (ESCs) are responsible for taking data from the gyroscope to decide which motor
takes more/less power to balance the quadcopter. Finally, and most obvious, the propellers are
set on top of the brushless motors to fly to drone. Figure 4.3 shows all those below.

```
Figure 4. 3 : Brushless Motors, ESCs, Propellers
```
**4. 2 .3 3S LiPo Battery 11.4V**
    The components used do use a big deal of power. However, to minimise costs it is
believed that a 3S LiPo Battery, shown in figure 4.4, will be enough to operate the quadcopter
for 2 – 5 minutes.

```
Figure 4. 4 : 3S LiPo Battery^
```

## 4. 2 .4 Arduino Uno R3

Figure 4.5 shows the Arduino Uno R3. It will operate as the flight controller as its job
will be to process signals coming in the control receiver that receives control commands from
the controller itself.

```
Figure 4. 5 : Arduino Uno R3
```
## 4. 2 .5 Mini Breadboard

Since the project will use an Arduino as the flight control a mini breadboard is essential
to use as the only way to connect the components to the Arduino is by using jumping wires and
connecting them via the breadboard. It is also worth mentioning that to minimise the weight of
the quadcopter, a mini breadboard should be considered. Figure 4.6 shows the mini breadboard
used in the project.

```
Figure 4. 6 : Mini Breadboard
```

**4. 2 .6 Gyroscope/Accelerometer MPU 6050**

Using a Gyroscope, Which is shown in figure 4.7, is essential as it will be the sensor that
will balance the quadcopter by calculating the angles it is at. After the calculation, it
communicates with the ESCs to decide which motor gets more/less power for balance.

```
Figure 4. 7 : Gyroscope/Accelerometer MPU 6050
```
## 4. 2 7 FlySky Controller and Receiver......................................................................

Figure 4.8 shows the FlySky controller which is the most suitable to use since there are
features in it that help control the quadcopter efficiently. It is also very compatible with
Arduinos.

```
Figure 4. 8 : FlySky Controller and Receiver RC
```

## 4. 2 .8 ESP32-CAM (Camera) with USB to TTL Converter

Using the ESP32-CAM camera for the First-person view is the best option. Since it has
many options for stream quality and speed. It has a built in Wi-Fi module to enable easy
connection through phones or laptops by connecting to the same Wi-Fi network and using its
IP address to view the stream and control the stream quality. The USB to TTL converter is used
to program the ESP32-CAM, without it, the camera will not function as desired. Both are
shown in figure 4.9 below.

```
Figure 4. 9 : ESP32-CAM and USB to TTL Converter^
```
**4. 2 .9 ESP32-WROOM-32U Wi-Fi and Bluetooth Module**

Figure 4.10 shows the Wi-Fi and Bluetooth module which is selected to be able to
broadcast the GPS’s module location when needed.

```
Figure 4. 10 : ESP32-WROOM-32U Wi-Fi and Bluetooth Module^
```

## 4. 2 10 GY-NEO6MV2 GPS Module

Choosing to use a GPS was for the possibility of losing the quadcopter due to any possible
control malfunctions such as: loss of signal, controller malfunction, control receiver
malfunctions, and many others. It uses the above-mentioned Wi-Fi module to broadcast its
location as long as the parties involved are connected to the same Wi-Fi network. Figure 4.11
shows the GPS module used.

```
Figure 4.1 1 : GY-NEO6MV2 GPS Module
```

**4.3 System Circuit**

```
This section will show and explain the circuitry of the quadcopter, camera, and GPS.
```
## 4. 3 .1 Quadcopter Circuit

As stated in Section 2.3, the project will use the YMFC-AL self-levelling drone circuit
schematic as a reference to the FPV drone in this project. Figure 4.12 shows the circuit diagram
of this project.

Figure 4.1 2 : Quadcopter Circuit Diagram
For power supply, the battery is connected to the frame which provides power to the
ESCs connected to the frame as well since the frame can be used as a conductor. Power is also
transmitted to the Arduino which then gives power to the other components (MPU 6050,
control receiver, GPS, and camera, Wi-Fi module) via the breadboard through the Vin, 5V, and
GND pins. The brushless motors are connected to the ESCs which are also connected to the
digital pins of the Arduino to receive information from the MPU 6050.

The MPU 6050 is connected to the 5V and GND pin from the Arduino via the mini
breadboard. The information pins are connected to the SDA and SCL pins in the Arduino
directly. The control receiver channels are directly connected to the Arduino digital pins. Power
supply for the receiver is also provided through the 5V and GND pins via mini breadboard.


## 4. 3 .2 ESP32-CAM Circuit

As stated in section 4. 2 .8, the ESP32-CAM has to be programmed via USB to TTL
converter and once that process is over, it only needs to be connected to power to operate.
Figure 4.13 shows the connection circuit of the ESP-CAM and the USB to TTL converter.

## Figure 4. 9 : ESP32-CAM and USB to TTL Converter

The USB to TTL converter provides power (5V and ground) to the ESP32-CAM during
the programming process along with the RX and TX connections for the programming itself.
Once the programming is done, power will need to be provided through the 5V and GND pins
via breadboard for operation.

## Figure 4.1 4 : GPS and Wi-Fi Module Circuit

Figure 4.1 4 : GPS and Wi-Fi Module Circuit
As mentioned earlier, The GPS and Wi-Fi module are connected as shown the figure
4.1 4. Both components get power from the Arduino via breadboard. The RX and TX of both
components are connected to each other as the Wi-Fi module broadcasts the information to the
user continuously through the same Wi-Fi network.


## 4 4 How the System Works

The controller is used to guide the drone by sending radio signals to the receiver which
is connected on the drone to the Arduino (the brain of the drone). The data from the receiver is
then processed in the flight controller code in the Arduino and it send signals to the ESCs which
then adjust the drone according to the instructions by using the motors and propellers.

The GPS and Camera modules are connected through coding to a Wi-Fi network which
the display device is also connected to. Since they are boards on their own, the have the
operation code saved in their memories so they only need to connect to power after coding.
The display is then shown by using the IP address of the camera through a webpage once the
IP address is entered as a URL. The location of the drone is collected through the same means.

**CHAPTER FIVE**


**PROGRAMMING OF THE SYSTEM**

The project’s programming includes two sections: a) Drone, and b) Camera, GPS, and
Wi-Fi. Programming of drone includes: i) Calibration of controller, receiver, and gyroscope,
ii) Calibration of ESCs and motor check, and iii) Flight controller code. The code also has
very important calculations that will be explained later in the chapter.

## 5 .1 Drone Programming..............................................................................................

## 5 .1.1 Calibration of Controller, Receiver, and Gyroscope

The first code calibrates the throttle, pitch, yaw, and roll of the controller and checks the
signal reception of the receiver as it gives detailed instruction on how to move the control sticks
to calibrate the controller. Once the control calibration is done, the code checks the address of
the gyroscope and also gives instruction on moving the quadcopter to set the values of the
angles to use once the quadcopter is in flight. After it calibrates and checks the values, it stores
them in the EEPROM in the Arduino to use with the third code.

## 5 .1.2 Calibration of ESCs and Controller, Gyroscope, and Motor Testing

The second code calibrates the ESCs and allows for motors to be checked for vibration
and weight issues to balance propellers individually and all together. It also allows for the
gyroscope angles to be checked (yaw, pitch, and roll) and checks the controller functionality
after calibration.

## 5.1. 3 Flight Controller Code

The Third code is the flight controller code. It takes the values stored from the EEPROM
and applies them to the variables used to control the quadcopter. The gyroscope reads the values
of its position and then instructs the ESCs to give more/less power to the motors for balance
and movement.

**5.2 Method of Calculation**


## 5. 2 .1 Calibration.......................................................................................................

## 5. 2 .1.1 Calculating the Position of the Control Sticks

As the value changes from HIGH to LOW in every pin that is assigned as input (in regard
to the pins connected to the receiver channels), the Interrupt Service Routine (ISR) is alerted,
and it interrupts whatever the Arduino is doing to run the ISR function in port B (pins from 9
to 13).

At the beginning of the ISR function the current running time is saved in microseconds
and after checking which pin initiated the interrupt, it checks if the pin states has changed from
HIGH to LOW or vice versa. In the case of LOW to HIGH, the timer for that channel signal is
set to the time of when the ISR function started running (current time) and exits the function.
The next time the pin state changes and enters the function, the previous pin state is saved as
HIGH.

_5. 2. 1 .2 Gyroscope Axis Calibration_

After starting the Gyroscope and the scaling to full scale 500 degree per second, the offset
of the gyroscope is calculated for each axis by taking 2000 readings from the gyro. Subtracting
each reading by the offset calculated for each axis, makes the angles more accurate. Each axis
value is divided by 2000 and subtracted from each new gyro readings for each axis. The new
gyro readings will be used at the calibration stage to determine the axis movement and in order
to determine the axis movement, measurement units need to be changed from radians/sec to
degree/sec by using the following equation:

_Axis in degrees = axis in radians * 0.0000611_
The number 0.000611 was calculated by the following:
(x/65.5)/R, where x = 1 radian, 65.5 is the value returned for each angular velocity change
per sec of an object in space, and R is 250 readings per sec to help make the data more accurate.
The values of the calibration are then stored in the EEPROM for later use.

_5.2.2 Calibration of ESCs and Controller and Gyroscope Testing_


## 5. 2 .2.1 Controller Testing and ESC Throttle Calibration

After retrieving the data from the EEPROM, the actual controller value must be
converted to the maximum and minimum range that is predetermined. If the actual controller
value is more than the maximum limit, the actual value is then set to that maximum value. The
same concept applies to the comparison of the actual value and the minimum limit.

There are 2 difference equations used to set the actual value to the correct range. The first
case where the receiver value is less than the centre value, the difference calculation takes place
as follows:

```
Difference = {(centre – actual) * 500} / (centre – LOW value from the calibration)
```
In case the channel was not reversed, 1500 is subtracted from the difference. Otherwise, the
1500 is added to the difference. The next case where the receiver value is more than the centre,
the difference is calculated as follows:

_Difference = {(actual – centre) * 500} / (HIGH value from the calibration – centre)_
Here if the channel is not reversed, 1500 is added. Otherwise, 1500 is subtracted. In case
the receiver value is equal to the centre value, the centre value is returned. When it comes to
displaying the controller test results, each channel value is compared to the centerpoint. If the
channel value being greater or less than the centerpoint, an arrow prints next to said value (up,
down, left, or right) to indicate the direction of the control sticks of said channel. Most ESC
calibration is done by sending a full throttle signal through the controller to synchronise the
ESC pulse to the motors and the controller signal.

_5.2.2.2 Gyroscope/Accelerometer Testing_


The user can test the axis by sending ‘a’ through the serial monitor to the Arduino. The
gyroscope testing starts by calling the gyro_signalen() function. The function starts by
accessing the MPU register where axis data can be read from. The code then requests 14 bytes
from the MPU that contains all access data including gyroscope and accelerometer access data.
The roll (x-axis) and pitch (y-axis) angle data is then converted to degrees/sec from radians/sec
by using the same conversion equation mentioned in section 5.2.1.2.

The pitch and roll angles are then integrated together with the yaw (z-axis) to influence
the change of direction for each axis. The following equation is used to solve the difference the
x and y axis output, and the actual x, y, z gyroscope location.

```
actual y-axis = converted y-axis – converted x-axis * sin (converted z-axis)
actual x-axis = converted x-axis + actual y-axis * sin (converted z-axis)
```
The yaw axis (z-axis) is converted from rad/sec to degree/sec by using the equation mentioned
in section 5.2.1.2 as the sine function needs rad/sec. The correction of the angle can be
represented in a circle. The current value (degree/sec) should be multiplied by π/180.

After the angle is calculated, it can be accurately represented by only using the gyroscope
data. However, the gyroscope data is affected by draft overtime which also contributed to by
the vibration of the motors as they operate. The accelerometer linear acceleration data should
be used to correct the draft, but if first needs to be converted from linear acceleration per second
(LA/S) to rad/sec by using the acceleration vector. The accelerometer data is useless under
vibration, so only a fraction of this data should be used and integrated with the majority of the
gyroscope data to solve the draft and vibration issues.

The acceleration vector can be calculated by taking the square root of the sum of the
square of each axis data from the accelerometer (Pythagorean theorem) as follows:

```
Acceleration vector = √(x-axis)^2 + (y-axis)^2 + (z-axis)^2
```
```
The inverse sine of the acceleration data divided by the acceleration vector results in a
```

radian acceleration value which is then multiplied by 57.296. Which is obtained by dividing
the linear acceleration data by π/180, to get the acceleration values in angles.

```
57.296 = linear acceleration data/(π/180)
Acceleration angle = sin-^1 (acceleration data/acceleration vector) * 57.296
```
Because the linear acceleration value for the x-axis is left-handed (reversed), unlike the right-
handed values of the rest of the axis, the radian value obtained by the inverse sin calculation
earlier, must be multiplied by -57.296.

_Acceleration angle (x-axis) = sin-_^1 _(acceleration data/acceleration vector) * -57.296_
When calibrated, the gyroscope is not guaranteed to be up-right, and the previous
gyroscope values affect the current calculated gyroscope values. Therefore, the first gyroscope
angle for each axis is assigned by the calculated accelerometer angle. Afterwards, each axis
angle is calculated by adding a fraction of the calculated accelerometer angle to a majority of
the calculated gyroscope angle. Example of calculation of one of the angles:

```
new angle pitch = angle pitch * 0.9996 + accelerometer pitch * 0.0004
```
Finally, the test results are displayed in the serial monitor of the Arduino IDE

## 5.2.2.3 Motor Testing and Propeller Balancing

16 acceleration vector values are readings are looped, added to the calculated acceleration
value, and then divided by 17 to get an average of the acceleration vector. A loop of 20 iterations
is then implemented where it subtracts the current acceleration vector from the average
acceleration vector calculated and takes the absolute value of the result of the subtraction. It is
then considered a vibration result. After the loop, the vibration result is then divided by 50 to
give more readable values in the display of said values in the serial monitor. This process is
executed for each motor individually.

_5.2.3 Flight Controller_


## 5.2. 3 .1 Controller

One of the fundamental concepts used in this project is the Proportional Integral
Derivative (PID), where each controller (P controller, I controller, and D controller) is
responsible for one function that would help directing the quadcopter. The controller results
are then combined to create a PID output. This operation is preformed for each axis separately.

In the case of the proportional controller, it calculates the difference between the
gyroscope angle and the receiver angle (the error), and then multiplies it by the proportional
gain as follows:

_proportional output = (gyroscope angle – receiver angle) * proportional gain_
The proportional controller can be described as the intensity of correcting the angle
accordingly. In the case of the integral controller, it calculates the difference between the
gyroscope angle and the receiver angle, multiplies it with the integral gain. and sums the result
to the previous integral output as follows:

_new integral output =
previous integral output + {(gyroscope angle – receiver angle) * integral gain}_
The integral controller can be described as the direction of correction of the angle. The
output of this controller is the opposite of the quadcopter angle. The proportional and integral
controllers can perform an angle correction but will overcorrect itself, as there is no friction
affecting the correction process. The derivative controller’s duty is to apply the friction required
to prevent the overcorrection process. It calculates the current difference between the
gyroscope angle and the receiver angle (current error), subtracts it from the previous error, and
then multiplies it by the derivative gain as follows;

```
derivative output = (current error – previous error) * derivative gain
```
The gains of each controller are modified as required.

After calculating the PID for each axis, the x, y, and z PIDs are added to or subtracted
from each ESC according to the individual motor location. It is important to have a gap (offset)
between the maximum range of the controller to be filled by the PID controllers to support
correction at full throttle.

_5.2.3.2 Modifying Motor Speed in Case of Voltage Drop_


The connection of the voltage divider circuit to the A0 analog pin of the Arduino is
responsible for reading the voltage and converting it to a value between 0 to 1023. 0 being the
minimum voltage and 1023 being the maximum voltage. A complementary filter is then used
to reduce electric noise caused by the varying input in voltage. For the new incoming readings
through analog pin A0, a high pass filter is used to preserve the high frequency information.
This value is then summed to the previous voltage reading which was also passed by a low
pass filter that is used to smooth out noise in the voltage readings.

_new voltage = previous voltage * low pass filter + (A0 reading + 65) * high pass filter_
The new battery voltage can be referred to as the battery level. In case of a voltage drop,
the buzzer starts beeping. Otherwise, the code checks if the battery voltage is under a certain
percentage. If it is, the code performs compensation on the pulse values of the ESCs by
increasing each pulse by a factor that is proportional to the difference between the desired
battery voltage and the measured battery voltage, using a scaling factor. The purpose of this
compensation is to account for the voltage drop of the battery and make sure the pulse values
accurately control the speed of the motors.

```
ESC n = ESC n * {(full voltage – current voltage) / adjustable scaling factor}
```
**5.3 Camera, GPS, and W-Fi Module Code Concept**


## 5. 3 .1 Camera Program and Display

While connected to the USB to TTL converter, the ESP32-CAM is programmed to
display the camera footage in a webpage that is created through its IP address when connected
to the same Wi-Fi network. Once programmed, the camera only needs to be connected to power
since it saves the code in its memory.

## 5. 3 2 GPS and Wi-Fi Program

As its primary purpose is to obtain its location, the GPS module is not programmed. This
statement implies that the GPS module's functionality is embedded or built-in, meaning that it
is an inherent component of the device or system in which it is used. Its embedded nature
allows it to perform its core function of retrieving location data without requiring additional
programming. However, to broadcast its position the Wi-Fi module is programmed to retrieve
whatever information the GPS module gets. Then the Wi-Fi module sends the information
through the Wi-Fi network.

**CONCLUSION**


In conclusion, FPV racing drones have emerged as an exciting and rapidly growing sport
that has gained popularity around the world. The immersive experience of flying a drone at
high speeds through obstacles and challenges has captivated the imagination of enthusiasts,
who are constantly pushing the limits of what is possible in this exciting sport. With
advancements in drone technology, including improvements in camera quality and drone
performance, the future of FPV racing drones looks bright.

At the same time, FPV racing drones have also raised some concerns around safety and
privacy. While the vast majority of pilots operate their drones responsibly and with respect for
the safety and privacy of others, there have been incidents of drones interfering with other
aircraft, causing damage, or infringing on people's privacy. As the sport continues to grow, it
will be important for pilots to follow safety guidelines and regulations, and for regulators to
ensure that appropriate measures are in place to mitigate any risks associated with drone use.
Overall, FPV racing drones are an exciting and dynamic field that is constantly evolving, and
it is expected to see many more exciting developments and achievements in the years to come.

**APPENDICIES**


**C: Flight Controller Code**

#include <Wire.h> //Include the Wire.h library to communicate with the
gyro.

#include <EEPROM.h> //Include the EEPROM.h library to store
information onto the EEPROM

### //////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

### /////////

//PID gain and limit settings
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
/////////

```
float pid_p_gain_roll = 0; //Gain setting for the roll P-controller
float pid_i_gain_roll = 0; //Gain setting for the roll I-controller
float pid_d_gain_roll = 0; //Gain setting for the roll D-controller
int pid_max_roll = 400; //Maximum output of the PID-controller
```
```
float pid_p_gain_pitch = pid_p_gain_roll; //Gain setting for the pitch P-controller.
float pid_i_gain_pitch = pid_i_gain_roll; //Gain setting for the pitch I-controller.
float pid_d_gain_pitch = pid_d_gain_roll; //Gain setting for the pitch D-controller.
int pid_max_pitch = pid_max_roll; //Maximum output of the PID-controller
```
```
float pid_p_gain_yaw = 0; //Gain setting for the pitch P-controller. //4.0
```

```
float pid_i_gain_yaw = 0; //Gain setting for the pitch I-controller. //0.02
float pid_d_gain_yaw = 0; //Gain setting for the pitch D-controller.
int pid_max_yaw = 400; //Maximum output of the PID-controller
```
```
boolean auto_level = true; //Auto level on (true) or off (false)
```
### //////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

### /////////

//Declaring global variables
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
/////////

byte last_channel_1, last_channel_2, last_channel_3, last_channel_4;
byte eeprom_data[36];
byte highByte, lowByte;
volatile int receiver_input_channel_1, receiver_input_channel_2,
receiver_input_channel_3, receiver_input_channel_4;

int counter_channel_1, counter_channel_2, counter_channel_3, counter_channel_4,
loop_counter;

```
int esc_1, esc_2, esc_3, esc_4;
int throttle, battery_voltage;
int cal_int, start, gyro_address;
int receiver_input[5];
int temperature;
int acc_axis[4], gyro_axis[4];
float roll_level_adjust, pitch_level_adjust;
```

long acc_x, acc_y, acc_z, acc_total_vector;
unsigned long timer_channel_1, timer_channel_2, timer_channel_3, timer_channel_4,
esc_timer, esc_loop_timer;

unsigned long timer_1, timer_2, timer_3, timer_4, current_time;
unsigned long loop_timer;
double gyro_pitch, gyro_roll, gyro_yaw;
double gyro_axis_cal[4];
float pid_error_temp;
float pid_i_mem_roll, pid_roll_setpoint, gyro_roll_input, pid_output_roll,
pid_last_roll_d_error;

float pid_i_mem_pitch, pid_pitch_setpoint, gyro_pitch_input, pid_output_pitch,
pid_last_pitch_d_error;

float pid_i_mem_yaw, pid_yaw_setpoint, gyro_yaw_input, pid_output_yaw,
pid_last_yaw_d_error;

```
float angle_roll_acc, angle_pitch_acc, angle_pitch, angle_roll;
boolean gyro_angles_set;
```
### //////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

### /////////

//Setup routine
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
/////////

```
void setup(){
Serial.begin(57600);
```

//Copy the EEPROM data for fast access data.
Serial.begin(57600);
//pinMode(13, OUTPUT);
for(start = 0; start <= 35; start++)eeprom_data[start] = EEPROM.read(start);
start = 0; //Set start back to zero.
gyro_address = eeprom_data[32]; //Store the gyro address
in the variable.

```
Wire.begin(); //Start the I2C as master.
```
TWBR = 12; //Set the I2C clock speed to
400kHz.

DDRD |= B11110000; //Configure digital poort 4, 5,
6 and 7 as output.

DDRB |= B00110000; //Configure digital poort 12
and 13 as output.

```
//Use the Buzzer on the Arduino for startup indication.
digitalWrite(12,HIGH); //Turn on the warning Buzzer.
```
```
set_gyro_registers(); //Set the specific gyro registers.
```
for (cal_int = 0; cal_int < 1250 ; cal_int ++){ //Wait 5 seconds before
continuing.

```
PORTD |= B11110000; //Set digital poort 4, 5, 6 and
```

7 high.

delayMicroseconds(1000); //Wait 1000us.
PORTD &= B00001111; //Set digital poort 4, 5, 6
and 7 low.

```
delayMicroseconds(3000); //Wait 3000us.
}
```
//Take multiple gyro data samples to determine the average gyro offset.
for (cal_int = 0; cal_int < 2000 ; cal_int ++){ //Take 2000 readings for
calibration.

if(cal_int % 15 == 0)digitalWrite(12, !digitalRead(12)); //Change the
Buzzer status to indicate calibration.

gyro_signalen(); //Read the gyro output.
gyro_axis_cal[1] += gyro_axis[1]; //Ad roll value to
gyro_roll_cal.

gyro_axis_cal[2] += gyro_axis[2]; //Ad pitch value to
gyro_pitch_cal.

gyro_axis_cal[3] += gyro_axis[3]; //Ad yaw value to
gyro_yaw_cal.

//stop the esc's from beeping annoyingly. give them a 1000us puls while calibrating
the gyro.

PORTD |= B11110000; //Set digital poort 4, 5, 6 and
7 high.

delayMicroseconds(1000); //Wait 1000us.
PORTD &= B00001111; //Set digital poort 4, 5, 6
and 7 low.

```
delay(3); //Wait 3 milliseconds before the next
```

loop.

}
//stop the esc's from beeping annoyingly. give them a 1000us puls while calibrating
the gyro.

gyro_axis_cal[1] /= 2000; //Divide the roll total by
2000.

gyro_axis_cal[2] /= 2000; //Divide the pitch total by
2000.

gyro_axis_cal[3] /= 2000; //Divide the yaw total by
2000.

PCICR |= (1 << PCIE0); //Set PCIE0 to enable
PCMSK0 scan.

PCMSK0 |= (1 << PCINT0); //Set PCINT0 (digital
input 8) to trigger an interrupt on state change.

PCMSK0 |= (1 << PCINT1); //Set PCINT1 (digital
input 9)to trigger an interrupt on state change.

PCMSK0 |= (1 << PCINT2); //Set PCINT2 (digital
input 10)to trigger an interrupt on state change.

PCMSK0 |= (1 << PCINT3); //Set PCINT3 (digital
input 11)to trigger an interrupt on state change.

//Wait until the receiver is active and the throtle is set to the lower position.
while(receiver_input_channel_3 < 990 || receiver_input_channel_3 > 1020 ||
receiver_input_channel_4 < 1400){

receiver_input_channel_3 = convert_receiver_channel(3); //Convert the
actual receiver signals for throttle to the standard 1000 - 2000us


receiver_input_channel_4 = convert_receiver_channel(4); //Convert the
actual receiver signals for yaw to the standard 1000 - 2000us

start ++; //While waiting increment start whith
every loop.

//stop the esc's from beeping annoyingly. give them a 1000us puls while calibrating
the gyro.

PORTD |= B11110000; //Set digital poort 4, 5, 6 and
7 high.

delayMicroseconds(1000); //Wait 1000us.
PORTD &= B00001111; //Set digital poort 4, 5, 6
and 7 low.

delay(3); //Wait 3 milliseconds before the next
loop.

```
if(start == 125){ //Every 125 loops (500ms).
digitalWrite(12, !digitalRead(12)); //Change the led status.
start = 0; //Start again at 0.
}
}
start = 0; //Set start back to 0.
```
```
//Load the battery voltage to the battery_voltage variable. TODO1
//65 is the voltage compensation for the diode.
//12.6V equals ~5V @ Analog 0.
//12.6V equals 1023 analogRead(0).
//1260 / 1023 = 1.2317.
//The variable battery_voltage holds 1050 if the battery voltage is 10.5V.
```

```
battery_voltage = (analogRead(0) + 65) * 1.2317;
```
loop_timer = micros(); //Set the timer for the next
loop.

//When everything is done, turn off the led.
digitalWrite(12,LOW); //Turn off the warning Buzzer.
}
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
/////////

//Main program loop
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
/////////

```
void loop(){
```
//65.5 = 1 deg/sec (check the datasheet of the MPU-6050 for more information).
gyro_roll_input = (gyro_roll_input * 0.7) + ((gyro_roll / 65.5) * 0.3); //Gyro pid
input is deg/sec.

gyro_pitch_input = (gyro_pitch_input * 0.7) + ((gyro_pitch / 65.5) * 0.3);//Gyro pid
input is deg/sec.

gyro_yaw_input = (gyro_yaw_input * 0.7) + ((gyro_yaw / 65.5) * 0.3); //Gyro pid
input is deg/sec.

```
//Gyro angle calculations
```

//0.0000611 = 1 / (250Hz / 65.5)
angle_pitch += gyro_pitch * 0.0000611; //Calculate the traveled
pitch angle and add this to the angle_pitch variable.

angle_roll += gyro_roll * 0.0000611; //Calculate the traveled
roll angle and add this to the angle_roll variable.

//0.000001066 = 0.0000611 * (3.142(PI) / 180degr) The sin function is in radians
angle_pitch -= angle_roll * sin(gyro_yaw * 0.000001066); //If the IMU has
yawed transfer the roll angle to the pitch angel.

angle_roll += angle_pitch * sin(gyro_yaw * 0.000001066); //If the IMU has
yawed transfer the pitch angle to the roll angel.

//Accelerometer angle calculations
acc_total_vector = sqrt((acc_x*acc_x)+(acc_y*acc_y)+(acc_z*acc_z)); //Calculate
the total accelerometer vector.

if(abs(acc_y) < acc_total_vector){ //Prevent the asin function
to produce a NaN

angle_pitch_acc = asin((float)acc_y/acc_total_vector)* 57.296; //Calculate the
pitch angle.

}
if(abs(acc_x) < acc_total_vector){ //Prevent the asin function
to produce a NaN

angle_roll_acc = asin((float)acc_x/acc_total_vector)* -57.296; //Calculate the
roll angle.

```
}
```

//Place the MPU-6050 spirit level and note the values in the following two lines for
calibration.

angle_pitch_acc -= 0.0; //Accelerometer calibration
value for pitch.

angle_roll_acc += 0.0; //Accelerometer calibration
value for roll.

angle_pitch = angle_pitch * 0.9996 + angle_pitch_acc * 0.0004; //Correct the
drift of the gyro pitch angle with the accelerometer pitch angle.

angle_roll = angle_roll * 0.9996 + angle_roll_acc * 0.0004; //Correct the drift
of the gyro roll angle with the accelerometer roll angle.

pitch_level_adjust = angle_pitch * 15; //Calculate the pitch
angle correction

roll_level_adjust = angle_roll * 15; //Calculate the roll angle
correction

if(!auto_level){ //If the quadcopter is not in auto-
level mode

pitch_level_adjust = 0; //Set the pitch angle correction
to zero.

roll_level_adjust = 0; //Set the roll angle correcion to
zero.

```
}
```
```
//For starting the motors: throttle low and yaw left (step 1).
```

if(receiver_input_channel_3 < 1050 && receiver_input_channel_4 < 1050)start = 1;
//When yaw stick is back in the center position start the motors (step 2).
if(start == 1 && receiver_input_channel_3 < 1050 && receiver_input_channel_4 >
1450){

```
start = 2;
```
angle_pitch = angle_pitch_acc; //Set the gyro pitch angle
equal to the accelerometer pitch angle when the quadcopter is started.

angle_roll = angle_roll_acc; //Set the gyro roll angle equal
to the accelerometer roll angle when the quadcopter is started.

```
gyro_angles_set = true; //Set the IMU started flag.
```
//Reset the PID controllers for a bumpless start.
pid_i_mem_roll = 0;
pid_last_roll_d_error = 0;
pid_i_mem_pitch = 0;
pid_last_pitch_d_error = 0;
pid_i_mem_yaw = 0;
pid_last_yaw_d_error = 0;
}
//Stopping the motors: throttle low and yaw right.
if(start == 2 && receiver_input_channel_3 < 1050 && receiver_input_channel_4 >
1950)start = 0;

```
//The PID set point in degrees per second is determined by the roll receiver input.
```

//In the case of deviding by 3 the max roll rate is aprox 164 degrees per second ( (500-
8)/3 = 164d/s ).

pid_roll_setpoint = 0;
if(receiver_input_channel_1 > 1508)pid_roll_setpoint = receiver_input_channel_1 -
1508;

else if(receiver_input_channel_1 < 1492)pid_roll_setpoint =
receiver_input_channel_1 - 1492;

pid_roll_setpoint -= roll_level_adjust; //Subtract the angle
correction from the standardized receiver roll input value.

pid_roll_setpoint /= 3.0; //Divide the setpoint for the
PID roll controller by 3 to get angles in degrees.

//The PID set point in degrees per second is determined by the pitch receiver input.
//In the case of deviding by 3 the max pitch rate is aprox 164 degrees per second (
(500-8)/3 = 164d/s ).

pid_pitch_setpoint = 0;
if(receiver_input_channel_2 > 1508)pid_pitch_setpoint = receiver_input_channel_2 -
1508;

else if(receiver_input_channel_2 < 1492)pid_pitch_setpoint =
receiver_input_channel_2 - 1492;

pid_pitch_setpoint -= pitch_level_adjust; //Subtract the angle
correction from the standardized receiver pitch input value.

pid_pitch_setpoint /= 3.0; //Divide the setpoint for the
PID pitch controller by 3 to get angles in degrees.


//The PID set point in degrees per second is determined by the yaw receiver input.
//In the case of deviding by 3 the max yaw rate is aprox 164 degrees per second (
(500-8)/3 = 164d/s ).

pid_yaw_setpoint = 0;
//We need a little dead band of 16us for better results.
if(receiver_input_channel_3 > 1050){ //Do not yaw when turning off the motors.
if(receiver_input_channel_4 > 1508)pid_yaw_setpoint = (receiver_input_channel_4 -
1508)/3.0;

else if(receiver_input_channel_4 < 1492)pid_yaw_setpoint =
(receiver_input_channel_4 - 1492)/3.0;

```
}
```
calculate_pid(); //PID inputs are known. So we
can calculate the pid output.

```
//The battery voltage is needed for compensation. TODO1
//A complementary filter is used to reduce noise.
//0.09853 = 0.08 * 1.2317.
battery_voltage = battery_voltage * 0.92 + (analogRead(0) + 65) * 0.09853;
```
```
//Turn on the led if battery voltage is to low.
if(battery_voltage < 1000 && battery_voltage > 600)digitalWrite(12, HIGH);
```

throttle = receiver_input_channel_3; //We need the throttle
signal as a base signal.

if (start == 2){ //The motors are started.
if (throttle > 1800) throttle = 1800; //We need some room to
keep full control at full throttle.

esc_1 = throttle - pid_output_pitch-2 + pid_output_roll - pid_output_yaw; //Calculate
the pulse for esc 1 (front-right - CCW)

esc_2 = throttle + pid_output_pitch-2 + pid_output_roll + pid_output_yaw;
//Calculate the pulse for esc 2 (rear-right - CW)

esc_3 = throttle + pid_output_pitch- 2 - pid_output_roll - pid_output_yaw; //Calculate
the pulse for esc 3 (rear-left - CCW)

esc_4 = throttle - pid_output_pitch- 2 - pid_output_roll + pid_output_yaw; //Calculate
the pulse for esc 4 (front-left - CW)

if (battery_voltage < 1240 && battery_voltage > 800){ //Is the battery
connected?

esc_1 += esc_1 * ((1240 - battery_voltage)/(float)3500); //Compensate the
esc-1 pulse for voltage drop.

esc_2 += esc_2 * ((1240 - battery_voltage)/(float)3500); //Compensate the
esc-2 pulse for voltage drop.

esc_3 += esc_3 * ((1240 - battery_voltage)/(float)3500); //Compensate the
esc-3 pulse for voltage drop.

esc_4 += esc_4 * ((1240 - battery_voltage)/(float)3500); //Compensate the
esc-4 pulse for voltage drop.

```
}
```

```
if (esc_1 < 1100) esc_1 = 1100; //Keep the motors running.
if (esc_2 < 1100) esc_2 = 1100; //Keep the motors running.
if (esc_3 < 1100) esc_3 = 1100; //Keep the motors running.
if (esc_4 < 1100) esc_4 = 1100; //Keep the motors running.
```
if(esc_1 > 2000)esc_1 = 2000; //Limit the esc-1 pulse to
2000us.

if(esc_2 > 2000)esc_2 = 2000; //Limit the esc-2 pulse to
2000us.

if(esc_3 > 2000)esc_3 = 2000; //Limit the esc-3 pulse to
2000us.

if(esc_4 > 2000)esc_4 = 2000; //Limit the esc-4 pulse to
2000us.

```
}
```
else{
esc_1 = 1000; //If start is not 2 keep a 1000us
pulse for ess-1.

esc_2 = 1000; //If start is not 2 keep a 1000us
pulse for ess-2.

esc_3 = 1000; //If start is not 2 keep a 1000us
pulse for ess-3.

esc_4 = 1000; //If start is not 2 keep a 1000us
pulse for ess-4.

```
}
```

//The refresh rate is 250Hz. That means the esc's need there pulse every 4ms.
while(micros() - loop_timer < 4000); //We wait until 4000us
are passed.

loop_timer = micros(); //Set the timer for the next
loop.

PORTD |= B11110000; //Set digital outputs 4,5,6
and 7 high.

timer_channel_1 = esc_1 + loop_timer; //Calculate the time of
the faling edge of the esc-1 pulse.

timer_channel_2 = esc_2 + loop_timer; //Calculate the time of
the faling edge of the esc-2 pulse.

timer_channel_3 = esc_3 + loop_timer; //Calculate the time of
the faling edge of the esc-3 pulse.

timer_channel_4 = esc_4 + loop_timer; //Calculate the time of
the faling edge of the esc-4 pulse.

```
gyro_signalen();
```
while(PORTD >= 16){ //Stay in this loop until
output 4,5,6 and 7 are low.

esc_loop_timer = micros(); //Read the current time.
if(timer_channel_1 <= esc_loop_timer)PORTD &= B11101111; //Set
digital output 4 to low if the time is expired.

if(timer_channel_2 <= esc_loop_timer)PORTD &= B11011111; //Set
digital output 5 to low if the time is expired.

```
if(timer_channel_3 <= esc_loop_timer)PORTD &= B10111111; //Set
```

digital output 6 to low if the time is expired.

if(timer_channel_4 <= esc_loop_timer)PORTD &= B01111111; //Set digital
output 7 to low if the time is expired.

```
}
}
```
//This routine is called every time input 8, 9, 10 or 11 changed state. This is used to read
the receiver signals.

ISR(PCINT0_vect){
current_time = micros();
//Channel 1=========================================
if(PINB & B00000001){ //Is input 8 high?
if(last_channel_1 == 0){ //Input 8 changed from 0 to 1.
last_channel_1 = 1; //Remember current input state.
timer_1 = current_time; //Set timer_1 to current_time.
}
}
else if(last_channel_1 == 1){ //Input 8 is not high and
changed from 1 to 0.

last_channel_1 = 0; //Remember current input state.
receiver_input[1] = current_time - timer_1; //Channel 1 is
current_time - timer_1.

### }

```
//Channel 2=========================================
```

if(PINB & B00000010 ){ //Is input 9 high?
if(last_channel_2 == 0){ //Input 9 changed from 0 to 1.
last_channel_2 = 1; //Remember current input state.
timer_2 = current_time; //Set timer_2 to current_time.
}
}
else if(last_channel_2 == 1){ //Input 9 is not high and
changed from 1 to 0.

last_channel_2 = 0; //Remember current input state.
receiver_input[2] = current_time - timer_2; //Channel 2 is
current_time - timer_2.

### }

//Channel 3=========================================
if(PINB & B00000100 ){ //Is input 10 high?
if(last_channel_3 == 0){ //Input 10 changed from 0 to
1.

last_channel_3 = 1; //Remember current input state.
timer_3 = current_time; //Set timer_3 to current_time.
}
}
else if(last_channel_3 == 1){ //Input 10 is not high and
changed from 1 to 0.

last_channel_3 = 0; //Remember current input state.
receiver_input[3] = current_time - timer_3; //Channel 3 is
current_time - timer_3.


### }

//Channel 4=========================================
if(PINB & B00001000 ){ //Is input 11 high?
if(last_channel_4 == 0){ //Input 11 changed from 0 to
1.

```
last_channel_4 = 1; //Remember current input state.
timer_4 = current_time; //Set timer_4 to current_time.
```
### }

### }

else if(last_channel_4 == 1){ //Input 11 is not high and
changed from 1 to 0.

last_channel_4 = 0; //Remember current input state.
receiver_input[4] = current_time - timer_4; //Channel 4 is
current_time - timer_4.

```
}
}
```
//reading the gyro
void gyro_signalen(){
//Read the MPU- 6050
Wire.beginTransmission(gyro_address); //Start communication
with the gyro.


Wire.write(0x3B); //Start reading @ register 43h
and auto increment with every read.

Wire.endTransmission(); //End the transmission.
Wire.requestFrom(gyro_address,14); //Request 14 bytes from
the gyro.

receiver_input_channel_1 = convert_receiver_channel(1); //Convert the
actual receiver signals for pitch to the standard 1000 - 2000us.

receiver_input_channel_2 = convert_receiver_channel(2); //Convert the
actual receiver signals for roll to the standard 1000 - 2000us.

receiver_input_channel_3 = convert_receiver_channel(3); //Convert the
actual receiver signals for throttle to the standard 1000 - 2000us.

receiver_input_channel_4 = convert_receiver_channel(4); //Convert the
actual receiver signals for yaw to the standard 1000 - 2000us.

while(Wire.available() < 14); //Wait until the 14 bytes are
received.

acc_axis[1] = Wire.read()<<8|Wire.read(); //Add the low and high
byte to the acc_x variable.

acc_axis[2] = Wire.read()<<8|Wire.read(); //Add the low and high
byte to the acc_y variable.

acc_axis[3] = Wire.read()<<8|Wire.read(); //Add the low and high
byte to the acc_z variable.

temperature = Wire.read()<<8|Wire.read(); //Add the low and high
byte to the temperature variable.

gyro_axis[1] = Wire.read()<<8|Wire.read(); //Read high and low
part of the angular data.

```
gyro_axis[2] = Wire.read()<<8|Wire.read(); //Read high and low
```

part of the angular data.

gyro_axis[3] = Wire.read()<<8|Wire.read(); //Read high and low
part of the angular data.

if(cal_int == 2000){
gyro_axis[1] -= gyro_axis_cal[1]; //Only compensate after
the calibration.

gyro_axis[2] -= gyro_axis_cal[2]; //Only compensate after
the calibration.

gyro_axis[3] -= gyro_axis_cal[3]; //Only compensate after
the calibration.

}
gyro_roll = gyro_axis[eeprom_data[28] & 0b00000011]; //Set gyro_roll
to the correct axis that was stored in the EEPROM.

if(eeprom_data[28] & 0b10000000)gyro_roll *= -1; //Invert gyro_roll
if the MSB of EEPROM bit 28 is set.

gyro_pitch = gyro_axis[eeprom_data[29] & 0b00000011]; //Set
gyro_pitch to the correct axis that was stored in the EEPROM.

// gyro_pitch = ((gyro_pitch*0.0000611)-2)/0.0000611;
if(eeprom_data[29] & 0b10000000)gyro_pitch *= -1; //Invert
gyro_pitch if the MSB of EEPROM bit 29 is set.

gyro_yaw = gyro_axis[eeprom_data[30] & 0b00000011]; //Set
gyro_yaw to the correct axis that was stored in the EEPROM.

if(eeprom_data[30] & 0b10000000)gyro_yaw *= -1; //Invert
gyro_yaw if the MSB of EEPROM bit 30 is set.


acc_x = acc_axis[eeprom_data[29] & 0b00000011]; //Set acc_x to the
correct axis that was stored in the EEPROM.

if(eeprom_data[29] & 0b10000000)acc_x *= -1; //Invert acc_x if
the MSB of EEPROM bit 29 is set.

acc_y = acc_axis[eeprom_data[28] & 0b00000011]; //Set acc_y to the
correct axis that was stored in the EEPROM.

if(eeprom_data[28] & 0b10000000)acc_y *= -1; //Invert acc_y if
the MSB of EEPROM bit 28 is set.

acc_z = acc_axis[eeprom_data[30] & 0b00000011]; //Set acc_z to the
correct axis that was stored in the EEPROM.

if(eeprom_data[30] & 0b10000000)acc_z *= -1; //Invert acc_z if the
MSB of EEPROM bit 30 is set.

```
}
```
```
//calculating pid outputs
void calculate_pid(){
//Roll calculations
pid_error_temp = gyro_roll_input - pid_roll_setpoint;
pid_i_mem_roll += pid_i_gain_roll * pid_error_temp;
if(pid_i_mem_roll > pid_max_roll)pid_i_mem_roll = pid_max_roll;
else if(pid_i_mem_roll < pid_max_roll * -1)pid_i_mem_roll = pid_max_roll * -1;
```
pid_output_roll = pid_p_gain_roll * pid_error_temp + pid_i_mem_roll +
pid_d_gain_roll * (pid_error_temp - pid_last_roll_d_error);

```
if(pid_output_roll > pid_max_roll)pid_output_roll = pid_max_roll;
else if(pid_output_roll < pid_max_roll * -1)pid_output_roll = pid_max_roll * -1;
```

```
pid_last_roll_d_error = pid_error_temp;
```
//Pitch calculations
pid_error_temp = gyro_pitch_input - pid_pitch_setpoint;
pid_i_mem_pitch += pid_i_gain_pitch * pid_error_temp;
if(pid_i_mem_pitch > pid_max_pitch)pid_i_mem_pitch = pid_max_pitch;
else if(pid_i_mem_pitch < pid_max_pitch * -1)pid_i_mem_pitch = pid_max_pitch * -
1;

pid_output_pitch = pid_p_gain_pitch * pid_error_temp + pid_i_mem_pitch +
pid_d_gain_pitch * (pid_error_temp - pid_last_pitch_d_error);

if(pid_output_pitch > pid_max_pitch)pid_output_pitch = pid_max_pitch;
else if(pid_output_pitch < pid_max_pitch * -1)pid_output_pitch = pid_max_pitch * -
1;

```
pid_last_pitch_d_error = pid_error_temp;
```
```
//Yaw calculations
pid_error_temp = gyro_yaw_input - pid_yaw_setpoint;
pid_i_mem_yaw += pid_i_gain_yaw * pid_error_temp;
if(pid_i_mem_yaw > pid_max_yaw)pid_i_mem_yaw = pid_max_yaw;
else if(pid_i_mem_yaw < pid_max_yaw * -1)pid_i_mem_yaw = pid_max_yaw * -1;
```
```
pid_output_yaw = pid_p_gain_yaw * pid_error_temp + pid_i_mem_yaw +
```

pid_d_gain_yaw * (pid_error_temp - pid_last_yaw_d_error);

```
if(pid_output_yaw > pid_max_yaw)pid_output_yaw = pid_max_yaw;
else if(pid_output_yaw < pid_max_yaw * -1)pid_output_yaw = pid_max_yaw * -1;
```
pid_last_yaw_d_error = pid_error_temp;
Serial.print("pid_output_roll: ");
Serial.print(pid_output_roll);
Serial.print("-- pid_output_pitch: ");
Serial.print(pid_output_pitch);
Serial.print("-- pid_output_yaw: ");
Serial.println(pid_output_yaw);
}
//convert the actual receiver signals to a standardized 1000 – 1500 – 2000 microsecond
value.

```
//The stored data in the EEPROM is used.
int convert_receiver_channel(byte function){
byte channel, reverse;
int low, center, high, actual;
int difference;
```
channel = eeprom_data[function + 23] & 0b00000111; //What channel
corresponds with the specific function

if(eeprom_data[function + 23] & 0b10000000)reverse = 1; //Reverse
channel when most significant bit is set

```
else reverse = 0; //If the most significant is not set
```

there is no reverse

actual = receiver_input[channel]; //Read the actual receiver
value for the corresponding function

low = (eeprom_data[channel * 2 + 15] << 8) | eeprom_data[channel * 2 + 14]; //Store
the low value for the specific receiver input channel

center = (eeprom_data[channel * 2 - 1] << 8) | eeprom_data[channel * 2 - 2]; //Store
the center value for the specific receiver input channel

high = (eeprom_data[channel * 2 + 7] << 8) | eeprom_data[channel * 2 + 6]; //Store
the high value for the specific receiver input channel

if(actual < center){ //The actual receiver value is
lower than the center value

if(actual < low)actual = low; //Limit the lowest value to
the value that was detected during setup

difference = ((long)(center - actual) * (long)500) / (center - low); //Calculate and
scale the actual value to a 1000 - 2000us value

if(reverse == 1)return 1500 + difference; //If the channel is
reversed

else return 1500 - difference; //If the channel is not
reversed

}
else if(actual > center){ //The actual
receiver value is higher than the center value

if(actual > high)actual = high; //Limit the lowest value to
the value that was detected during setup

difference = ((long)(actual - center) * (long)500) / (high - center); //Calculate and
scale the actual value to a 1 000 - 2000us value


if(reverse == 1)return 1500 - difference; //If the channel is
reversed

else return 1500 + difference; //If the channel is not
reversed

```
}
else return 1500;
}
```
void set_gyro_registers(){
//Setup the MPU- 6050
if(eeprom_data[31] == 1){
Wire.beginTransmission(gyro_address); //Start
communication with the address found during search.

Wire.write(0x6B); //write to the PWR_MGMT_1
register (6B hex)

Wire.write(0x00); //Set the register bits as
00000000 to activate the gyro

Wire.endTransmission(); //End the transmission with
the gyro.

Wire.beginTransmission(gyro_address); //Start
communication with the address found during search.

Wire.write(0x1B); //write to the
GYRO_CONFIG register (1B hex)

Wire.write(0x08); //Set the register bits as
00001000 (500dps full scale)

Wire.endTransmission(); //End the transmission with
the gyro


Wire.beginTransmission(gyro_address); //Start
communication with the address found during search.

Wire.write(0x1C); //write to the
ACCEL_CONFIG register (1A hex)

Wire.write(0x10); //Set the register bits as
00010000 (+/- 8g full scale range)

Wire.endTransmission(); //End the transmission with
the gyro

//check to see if the values are written correct
Wire.beginTransmission(gyro_address); //Start
communication with the address found during search

Wire.write(0x1B); //Start reading @ register
0x1B

Wire.endTransmission(); //End the transmission
Wire.requestFrom(gyro_address, 1); //Request 1 bytes from
the gyro

while(Wire.available() < 1); //Wait until the 6 bytes are
received

if(Wire.read() != 0x08){ //Check if the value is 0x08
digitalWrite(12,HIGH); //Turn on the warning led
while(1)delay(10); //Stay in this loop for ever
}
Wire.beginTransmission(gyro_address); //Start
communication with the address found during search

Wire.write(0x1A); //write to the CONFIG register
(1A hex)

```
Wire.write(0x03); //Set the register bits as
```

00000011 (Set Digital Low Pass Filter to ~43Hz)

Wire.endTransmission(); //End the transmission with
the gyro

```
}
}
```

**REFERENCES**

[1] 3-D Printed Drone:

https://www.pmu.edu.sa/attachments/academics/pdf/udp/coe/dept/me/fall2020_2021/3d_print
ed_drone_report.pdf

## Figure 2.1: Drone for Civil Applications

https://core.ac.uk/download/pdf/61806036.pdf

[3] YMFC-AL Self-levelling drone:

[http://www.brokking.net/ymfc-al_main.html](http://www.brokking.net/ymfc-al_main.html)
