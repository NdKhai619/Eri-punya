# Real-Time IoT Energy Monitoring System for Residential Applications Using ESP32 and PZEM-004T Sensors

Muhammad Zulhairi Bin Suhaimey  
Faculty of Electrical and Electronic Engineering Technology  
Universiti Malaysia Pahang  
Pekan, Pahang, Malaysia  
zulhairiery14@gmail.com  

TS. Muhamad Ridzuan Bin Radin Muhamad Amin  
Faculty of Electrical and Electronic Engineering Technology  
Universiti Malaysia Pahang  
Pekan, Pahang, Malaysia  

**Abstract**—This project designs and implements a real-time IoT energy monitoring system for residential applications using ESP32 microcontrollers with PZEM-004T sensors and CT clamps, achieving high measurement accuracy (voltage: ±0.5%, current: ±0.5%). The system streams data to Home Assistant, providing intuitive dashboards to visualize circuit-level consumption patterns, including peak demand periods (1.6 kWh at 10 AM) and standby power waste (0.2 kWh overnight). Key innovations are a custom PCB for long-lasting multi-sensor integration and a 3D-printed enclosure for deployable scaling. Outcomes include: (1) measurement precision on par with commercial hardware, (2) identification of energy-saving potential through comprehensive load profiling, and (3) open-source residential energy management platform. Future improvements could involve monitoring renewable energy or predictive analytics. The project verifies low-cost IoT ideas as strong tools for energy awareness and efficiency within the home.

**Index Terms**—IoT energy monitoring, ESP32, PZEM-004T, CT clamp, Home Assistant, real-time power measurement, energy efficiency, custom PCB, 3D-printed enclosure, open-source framework.

## I. INTRODUCTION

The integration of Internet of Things (IoT) technologies is among the many integral components in assisting with the changes of traditional systems to smarter and more efficient solutions, especially in energy management IoT has come to. Modern day challenges like sustainability, conserving energy, and the global electricity cost have driven a lot of interest towards autonomy and intelligent home systems [1]. Conclusively, the goal of this project is to develop an all-encompassing system capable of monitoring energy consumption in real time through IoT technologies accurately tailored for residential use. The system is built around an ESP32 microcontroller which is very effective in smart home IoT communication due to its dual core processor, low power use, Wi-Fi, and Bluetooth capabilities. The aim of this project is to develop an accurately tailored IoT energy monitoring system for residential usage [2]. Coupled with the PZEM-004T sensors module and its kWh measuring capabilities, the system will precisely and continuously monitor electrical circuits ranging from voltage, current, power, frequency, power factor, and energy calculation. The sensors are positioned over multiple Miniature Circuit Breakers (MCBs) to obtain more precise details than the basic level of a household and gain deeper insights regarding energy consumption at the circuit level, allowing for analysis of what region or device is consuming more power [6]. Each sensor's data is downloaded to a central repository and visualized with the help of Home Assistant, which is a free home automation software featuring a self-configurable dashboard. Users can monitor their energy consumption in real-time with the aid of dynamic graphs, charts, and gauge meters, receive notifications in case of unusual energy consumption and current flow, and monitor long-term trends which can later support their decision to save energy. Unlike traditional energy meters, which provide aggregate and summary data, this system provides users with remote access and effortless control, enabling them to monitor their energy consumption from their smartphones or personal computers, making it exceptional. This project improves the safety and efficiency of energy systems within the household, and, when considered alongside the low costs of the hardware and sensors, powerful visualization tools, shifts the project's focus towards the overarching aims of smart grid advancement, eco-friendly development, and smart energy management, making it a worthwhile investment for the future.

## II. RELATED WORKS

### A. Smart Energy Meter Using IoT for Monitoring and Billing System

This paper focuses on the design of an IoT-based smart energy meter system that guarantees real-time and efficient monitoring of electrical energy consumption in home environments. The focus of the system is the ESP32 microcontroller, which has native Wi-Fi capability, offering efficient wireless transmission and internet connectivity for remote monitoring. The measurement of the energy is done by the PZEM-004T sensor module, which was chosen for its capability to measure some crucial electrical parameters like voltage, current, frequency, power factor, and total energy consumption in kilowatt-hours (kWh) units [3].

The system is designed to make these measurements in real-time and transfer them to a web-based dashboard that is cloud-enabled. This interface allows consumers to see patterns in energy usage, compare past consumption rates, and monitor real-time values. One added feature of this system is the inclusion of an integrated billing mechanism that determines the amount of electricity consumed based on a pre-established tariff model. This allows the consumer to have more knowledge about their electricity bill and be able to schedule usage accordingly. Furthermore, the system sends notification warnings for abnormal patterns of consumption, such as sudden spikes in power usage or potential device malfunction, thereby increasing the security and energy efficiency of the dwelling.

Compared to typical analog meters, which can only provide cumulative values and need to be read manually, this smart meter enables automatic, real-time data regarding energy usage through any internet-enabled device. The use of low-cost, off-the-shelf hardware such as ESP32 and PZEM-004T makes the system extremely cost-effective and scalable for mass deployment in residential communities. Even though the interface utilized is an in-house web-based dashboard rather than a home automation platform such as Home Assistant, the overall system architecture demonstrates a high level of flexibility with modern-day smart home energy solutions. It shows the ability of IoT to support open energy management, stimulate awareness among consumers, and support sustainable consumption by data-based decision-making.

### B. IoT-Based Real-Time Energy Monitoring Using ESP32 and Blynk

This paper presents the development of an IoT-based real-time energy monitoring system in a home environment. The system is built around the ESP32 microcontroller, chosen due to its dual-core processing, low power consumption, and on-board Wi-Fi capability, making it highly suitable for wireless IoT projects. The PZEM-004T module is used as the primary energy measurement sensor in the system. This sensor enables accurate detection and measurement of different electrical parameters like voltage, current, active power, frequency, and total energy consumed [4]. These electrical measurements in real-time are periodically read by ESP32 and transmitted wirelessly to the Blynk platform over the internet.

The Blynk app, which is designed to work with mobile interfaces, acts as the primary dashboard for data visualization, offering real-time feedback in the form of graphical charts, gauges, and notifications. This allows end-users to monitor and learn their energy consumption habits at convenience from their smartphones. The system is designed with simplicity of installation and cost-effectiveness in mind, making it extremely well-suited for average household users looking to reduce their electricity usage and enhance home energy efficiency. Furthermore, the installation offers customizable self-programmable alert features, such as alerts for irregular power usage or overcurrent status, to assist in safety and operational awareness of home electrical systems.

The project framework also offers remote monitoring and control, allowing consumers to keep track of their energy usage from nearly any place, assisting proactive energy conservation behaviors. Although the system uses Blynk for IoT visualization instead of platforms like Home Assistant, the use of the ESP32 and PZEM-004T combination still shows a feasible, scalable solution to real-time energy data gathering and visualization. The project demonstrates the potential for using cloud-based mobile interfaces in low-cost energy monitoring systems, empowering the field of smart energy management through increased energy awareness and behavioral-based savings in residential energy consumption.

### C. Home Energy Management System Based on IoT Using ESP32 and MQTT

This work demonstrates an end-to-end IoT-based Home Energy Management System (HEMS) for energy consumption monitoring and control of multiple circuits within a domestic setting. The system revolves around the ESP32 microcontroller because of its robust processing capabilities and embedded wireless connectivity. Non-invasive current transformers such as the SCT-013 are used for current measurements across various home power lines. These sensors provide analog output values proportional to current flow, which are subsequently calculated by the ESP32 to arrive at real-time power consumption data. As for communication, the system utilizes the Message Queuing Telemetry Transport (MQTT) protocol, a lightweight and efficient messaging protocol ideal for IoT application. The readings from the ESP32 are published to an MQTT broker, which forwards the same to subscribing devices, including a dashboard interface that shows electrical usage trends for different zones in the home [5].

The dashboard enables in-depth and interactive graphical representation of consumption patterns, allowing residents to monitor, compare, and analyze power consumption real-time. For safety monitoring, the installation also has fault detection and power surge alerts, which enhance the dependability and responsiveness of the installation. Alerts are produced upon the detection of anomalies, and thus, users can intervene on time and prevent risks or equipment malfunction. Designed with scalability in mind, the system can be able to incorporate additional sensors and circuits, allowing it to be adaptable to different home environments and power supply systems. Although the implementation utilizes SCT-013 sensors and MQTT in place of PZEM-004T and Home Assistant, the project's core objective is to deliver a circuit-level real-time energy monitoring system with remote visualization and intelligent feedback is greatly applicable to other architectures of smart energy management. The focus on modular integration, expansion simplicity, and real-time monitoring makes this system an asset to the development of effective and user-friendly home energy monitoring systems.

## III. RESEARCH METHODOLOGY

### A. Real-Time Energy Monitoring System Design

#### 1) Hardware Components

- **Microcontroller:** ESP32 (flashed with Tasmota for PZEM-004T/CT clamp integration).
- **Sensors:**
  - PZEM-004T: Measures voltage (80–260V) and frequency (45–65Hz) directly.
  - External CT Clamps (OPCT10AL): Measure current (0–100A) for power (W), energy (kWh), and power factor.
- **Communication:** MQTT (Mosquitto broker) for efficient data transmission.
- **Server:** Raspberry Pi 5 hosting Node-RED for data processing and visualization.

#### 2) Software Workflow

**Data Acquisition:**
- PZEM-004T reads voltage(V), frequency (Hz), while CT clamp measures current (A), power (W), power factor and energy (kwh).
- ESP32 (Tasmota) processes data and publishes MQTT topics for example (MQT:tele/RealTimeEnergyMonitoring/SENSOR).

**Real-Time Visualization:**
- Home Assistant subscribes to MQTT topics and displays data on a dynamic dashboard (gauges, graphs, and tables).

**Energy Efficiency:**
- MQTT's lightweight publish-subscribe model minimizes ESP32 energy consumption.

#### 3) Validation

- Compare OPCT10AL CT clamp current readings with a clamp meter (error < ±1%).
- Validate PZEM-004T voltage measurements against multimeter.

*[Space for Figure 1: Testing the accuracy of the sensor using AC/DC Clamp Meter]*

### B. Cloud Server Deployment on Raspberry Pi

#### 1) Home Assistant Setup

- Install Home Assistant OS on Raspberry Pi 5.
- Add Mosquitto MQTT broker (for ESP32 communication) via add-ons [7].

#### 2) Data Integration

- ESP32 (Tasmota) sends PZEM-004T + CT clamp data to MQTT topics.
- Home Assistant auto-discovers sensors or imports them via YAML.

#### 3) Security & Access

- Enable TLS for MQTT.
- Use HA's built-in user roles for access control.

### C. Data Accessibility and Security

#### 1) Energy Dashboard

- Leverage Home Assistant's built-in Energy Dashboard to visualize:
  - Real-time power consumption per circuit.
  - Historical trends (daily/monthly).

#### 2) Encryption

- Enable TLS for Mosquitto MQTT (via Home Assistant add-on configuration).

### D. Working Flow

*[Space for Figure 2: Working Flow of the system]*

The system begins by capturing electrical parameters from the residential circuits. The PZEM-004T sensors measure voltage and frequency directly from the AC mains, while external CT clamps monitor current flow through each circuit. These raw measurements are transmitted to the ESP32 microcontroller, which runs Tasmota firmware to process the data. The ESP32 calculates critical metrics like active power (W), energy consumption (kWh), and power factor by combining voltage readings from the PZEM with current data from the CT clamps.

Processed data is published via the MQTT protocol (using Mosquitto broker) to ensure lightweight, real-time communication. Raspberry Pi 5 acts as the central hub, hosting the MQTT broker and Home Assistant. Home Assistant either auto-discovers the Tasmota devices or maps them manually via YAML configurations. This step ensures seamless integration of all sensors into a unified dashboard.

Home Assistant's Lovelace UI displays real-time metrics through customizable gauges, graphs, and circuit-specific breakdowns. Users can access this dashboard from computers, smartphones, or tablets, with responsive design for cross-device compatibility.

To ensure robustness, the ESP32's Tasmota firmware includes Wi-Fi recovery mechanisms, while MQTT's QoS guarantees data delivery. Future scalability is supported by adding more PZEM/CT pairs without hardware overhauls.

### E. Hardware Design

#### 1) Custom PCB

**Core Functionality:**
- Interfaces ESP32 with PZEM-004T sensors via GPIO pins (D16-D17, D21-D22) for voltage/current measurement.
- Includes AC/DC isolation to protect low-voltage components.

**Key Features:**
- Optimized trace routing to minimize noise (critical for accurate analog measurements).
- Labeled test points for example VIN, GND for debugging.
- Compact form factors for enclosure compatibility.

*[Space for Figure 3: PCB layout for connection and power sections]*

#### 2) 3D-Printed Enclosure

**Design Rationale:**
- Houses PCB + PZEM-004T + CT clamps with slots for cable management.
- Ventilation channels to prevent overheating.

**Material:**
- Material: PETG for balance of cost and durability.
- Wall-mount design: Screw holes/stands for field deployment.

*[Space for Figure 4: 3D model showing component placement and access ports]*

## IV. RESULTS AND DISCUSSION

### A. System Integration and Visualization

This study highlights how Home Assistant effectively converts IoT power monitoring data into actionable insights. The platform's user-friendly dashboards tidily present consumption patterns, identifying points of peak usage (1.6 kWh at 10 AM) and idle losses (0.2 kWh at night). With the addition of PZEM-004T and CT clamp readings, Home Assistant presents real-time circuit-level monitoring while calculating daily costs (MVR 2.52). The research demonstrates how such synergy of precise sensing and user-friendly interfaces enables homeowners to achieve maximum energy efficiency through data-driven decisions, substantiating the system's value in real-world household energy management. The seamless ESP32-to-Home Assistant integration is particularly useful in tracking usage behaviors and identifying savings opportunities.

*[Space for Figure 5: Home Assistant interface]*

### B. Voltage Monitoring Results

The experimental results demonstrate the effectiveness of the IoT-based energy monitoring system in capturing detailed residential power consumption patterns. As shown in the voltage monitoring graph, the system maintained precise measurements across five circuits (L1-L5), recording stable voltages between 243.5V and 246.5V over a 70-minute period, with minimal fluctuations of just ±1.2%. This high level of accuracy confirms the reliability of the PZEM-004T sensors for residential applications.

*[Space for Figure 6: Voltage graph from 12am to 1:30am]*

### C. Current and Power Consumption Analysis

The current consumption data reveals distinct load profiles, with Circuit 3 showing characteristic peak demand periods during early morning (4:00-6:00 AM) and evening (6:00-8:00 PM), while Circuits 1 and 5 exhibited persistent low-current consumption indicative of standby power waste. Power consumption analysis showed significant variation throughout the day, peaking at 1,000W during afternoon hours when multiple appliances operated simultaneously, while maintaining a baseline of 200-400W overnight.

*[Space for Figure 7: Current graph from L1 to L5]*

*[Space for Figure 8: Power graph from L1 to L5]*

### D. Daily Energy Consumption Patterns

Residential energy consumption patterns provide critical insights for optimizing electricity usage and reducing costs. Figure 6 illustrates a typical day's consumption profile, revealing distinct peaks and troughs in energy demand. Key observations from the data include morning (6:00–10:00 AM) and evening (6:00–10:00 PM) usage spikes, reaching 1.4–1.6 kWh, coinciding with household activities like cooking and appliance use. Conversely, overnight consumption drops sharply to 0.2–0.5 kWh, highlighting opportunities to minimize standby power waste. This analysis underscores the potential for behavioral adjustments and tariff optimization to achieve measurable savings. By correlating these patterns with circuit-level data from the IoT monitoring system, homeowners can target high-demand appliances and implement automated energy-saving measures [9].

*[Space for Figure 9: Energy consumption for one day]*

### E. Performance Evaluation

[To be filled later]

### F. Cost-Benefit Analysis

[To be filled later]

## V. CHALLENGES AND LIMITATIONS

### A. Technical Challenges

[To be filled later]

### B. Implementation Challenges

[To be filled later]

### C. Scalability Considerations

[To be filled later]

## VI. FUTURE WORK

### A. System Enhancements

[To be filled later]

### B. Advanced Analytics Integration

[To be filled later]

### C. Renewable Energy Integration

[To be filled later]

## VII. CONCLUSION

This work successfully designed and evaluated an IoT-supported real-time energy monitoring system integrated with ESP32 microcontrollers with PZEM-004T sensors and CT clamps, with accurate voltage (±0.5%) and current (±0.5%) measurement. The system's custom PCB design facilitated efficient multi-circuit monitoring through optimized signal integrity, and its 3D-printed enclosure provided an easy-to-deploy, modular solution. Through Home Assistant integration, the system effectively translated raw sensor measurements into actionable intelligence, identifying peak usage hours (1.6 kWh at 10 AM) and standby power loss (0.2 kWh at night) that enable cost-saving actions. The software-hardware interface was particularly well-suited to bridge technology measurements with human-scale visualization for domestic energy management. This project makes available a replicable example for low-cost, open-source energy monitoring systems that provide residents with data-driven gains in efficiency.

## ACKNOWLEDGMENT

First and foremost, I would like to express my deepest gratitude to my dedicated supervisor, Ts. Muhamad Ridzuan Bin Radin Muhammad Amin, whose unwavering guidance, technical expertise, and patient mentorship were instrumental in shaping this project from conception to completion. His insightful feedback during our consultations not only resolved critical challenges but also inspired me to refine both the theoretical framework and practical implementation of this research.

I am equally thankful to the faculty members who supported my work which is Mr. Danial Nuqman Bin Khairul Nizam, Mr. Muhammad Ameer Bin Nor Sharudin, Mr. Muhammad Sollehin Bin Shajurudin, and Mr. Hakimi Ikhwan Bin Mohd Azhar for their technical advice, laboratory support, and encouragement throughout my academic journey.

To my family and friends, your unwavering belief in me, patience during long hours of work, and words of encouragement became the foundation that sustained my motivation. This achievement is as much yours as it is mine. I acknowledge University Malaysia Pahang Al-Sultan Abdullah (UMPSA) for providing the resources and environment that made this research possible.

Last but not least, I want to thank me, I want to thank me for believing in me, I want to thank me for doing all this hard work, I want to thank me for having no days off, I want to thank me for, for never quitting, I want to thank me for always being a giver And try to give more than I receive, I want to thank me for tryna do more right than wrong, I want to thank me for just being me at all times.

## REFERENCES

[1] Affum, E. A., Agyeman-Prempeh, K., Adumatta, C., Ntiamoah-Sarpong, K., & Dzisi, J. (2021). Smart Home Energy Management System based on the Internet of Things (IoT). *International Journal of Advanced Computer Science and Applications*, 12(2). https://doi.org/10.14569/ijacsa.2021.0120290

[2] Al-Fuqaha, A., Guizani, M., Mohammadi, M., Aledhari, M., & Ayyash, M. (2015). Internet of Things: A Survey on Enabling Technologies, Protocols, and Applications. IEEE Communications Surveys & Tutorials, 17(4), 2347–2376.

[3] Iot Based Smart Energy Meter Monitoring and Billing System. (2020). International Journal of Innovative Technology and Exploring Engineering, 9(4), 1480–1483. https://doi.org/10.35940/ijitee.f4301.049620

[4] Alam, M. (2020, November 30). IoT Based Electricity Energy Meter using ESP32 & Blynk. How to Electronics. https://how2electronics.com/iot-based-electricity-energy-meter-using-esp32-blynk/

[5] Li, H., Lu, L., & Yu, M. (2023). Home Energy Management System (HEMS) Based on Non-Intrusive Load Monitoring. 2023 IEEE 7th Conference on Energy Internet and Energy System Integration(EI2),3547–3552. https://doi.org/10.1109/ei259745.2023.10512886

[6] Gopika, B., Tech, C., Dept, George, S., & Dept, C. (2021). IoT Based Smart Energy Management System using Pzem-004t Sensor & Node MCU. https://www.ijert.org/research/iot-based-smart-energy-management-system-using-pzem-004t-sensor-node-mcu-IJERTCONV9IS07011.pdf

[7] Usmani, M. F. (2021, May 21). MQTT Protocol for the IoT - Review Paper. ResearchGate. https://doi.org/10.13140/RG.2.2.26065.10088

[8] Munoz, O., Ruelas, A., Rosales, P., Acuña, A., Suastegui, A., & Lara, F. (2022). Design and Development of an IoT Smart Meter with Load Control for Home Energy Management Systems. Sensors,22(19),7536. https://doi.org/10.3390/s22197536

[9] Kamolwan Wongwut, & Daungkamol Angamnuaysiri. (2024). development of real-time energy monitoring system using IoT base. Journal of Applied Research on Science and Technology (JARST). https://doi.org/10.60101/jarst.2024.255911