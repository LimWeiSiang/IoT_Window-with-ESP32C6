# IoT Window Control and Automatic Rain Detection project for 30.201 Wireless Communications and Internet of Things

# IoT Window Control and Automatic Rain Detection
This is a project for IoT Window Control and Automatic Rain Detection. The project utilizes the ESP32C6 Dev Board from Espressif and the Rainmaker App to operate and automate a smart home window. The primary functionalities enable users to remotely open and close their smart home windows via the app. The distinctive feature of this project is its ability to notify, detect and autonomously close the window when it is raining.

# Project Github Repository
https://github.com/LimWeiSiang/IoT_Window-with-ESP32C6

# Getting started with Project (Installation)
<p>Step 1:
Git clone IoT Window Control and Automatic Rain Detection repository https://github.com/LimWeiSiang/IoT_Window-with-ESP32C6.git into "C:/Espressif/framework/esp-rainmaker/examples/".
<br>
<br>Step 2
Open “IoT_Window-with-ESP32C6” folder with Visual Studio Code. Initialize COM port and device in Visual Studio Code. Select ESP32C6 as your target board.
<br>
<br>Step 3:
Download the ESP RainMaker App from the App Store or Google Play Store.
<br>
<br>Step 4:
Build and flash the project to the ESP32C6 board using Visual Studio Code. A QR code would be generated on the monitor terminal. Scan it with the ESP Rainmaker App. 
</p>

# Project Schematic
The following schematic shows the GPIO pins used for the various components.
<br>
![Project Schematic](https://github.com/LimWeiSiang/IoT_Window-with-ESP32C6/blob/main/BOM%20and%20Schematics/Project%20Schematic%20and%20Wiring%20Diagram.png?raw=true)


# Project Hardware Setup
<p>Step 1: Insert the 3D printed window frame onto MG996R Metal Gear Servo as shown on the left figure. Secure with M3x6 fastener that is provided with the servo.

  ![3D printed window frame onto MG996R Metal Gear Servo](https://github.com/LimWeiSiang/IoT_Window-with-ESP32C6/blob/main/CAD%20Models/Frame%20Assem.PNG?raw=true)

<br>Step 2: Slot the assembled window frame servo into the 3D printer Holder Mount as shown below. Place the breadboard and other components onto the Holder Mount.
![assembled window frame servo into the 3D printer Holder Mount](https://github.com/LimWeiSiang/IoT_Window-with-ESP32C6/blob/main/CAD%20Models/Holder%20assem.PNG?raw=true)

</p>


# Project Device Behaviour
<p>
The primary function of opening and closing the window can be done via two methods. The first would be via the physical push button. The second would be via the RainMaker App. When toggled the “Servo Switch” element on the app would display change. In addition, the app would notify the user of the current operation via notification.
</p>

![Project Device Behaviour Image 1](https://github.com/LimWeiSiang/IoT_Window-with-ESP32C6/blob/main/Device%20Behaviour%20Image/Device%20Behaviour%201.png?raw=true)


<p>
The distinctive feature of notifying, detecting and autonomously closing the window when it is raining. To demonstrate this behaviour the moisture sensor is dipped into a small pool of water on the right of the Holder Mount. The “Rain Sensor” element on the app will change its state from 0 to 1 to represent rain is detected. After 10 seconds the window is automatically closed. The adjustable 10 second period is to prevent false detection. Furthermore, two alerts "🌧 Its Raining!!! 🌧" and “Auto Closing Window” will appear on the User’s mobile device. This ensures the user is always informed about the state of their smart window.

  ![Project Device Behaviour Image 2](https://github.com/LimWeiSiang/IoT_Window-with-ESP32C6/blob/main/Device%20Behaviour%20Image/Device%20Behaviour%202.png?raw=true)
</p>

<p>
Lastly, a safety feature where the device will not close the window if the micro switch or limit switch is pressed. To showcase this behaviour, the limit switch is purposely depressed when the window is in the open position. When it is depressed the “Limit Switch Device” element on the app will change its state from 0 to 1. When the user tries to close the window the device will not close and instead, a “Not Closing! Limit Switch is Pressed!” notification will be displayed on the user’s device.

  ![Project Device Behaviour Image 3](https://github.com/LimWeiSiang/IoT_Window-with-ESP32C6/blob/main/Device%20Behaviour%20Image/Device%20Behaviour%203.png?raw=true)
</p>
</p>
