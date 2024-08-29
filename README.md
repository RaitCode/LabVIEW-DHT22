# LabVIEW-DHT22

Project involves using a DHT22 or DHT11 sensor connected to an Arduino Uno to acquire temperature and humidity data. This data is then transmitted to a LabVIEW program via the VISA serial communication interface. The LabVIEW program not only displays the data in real-time on a graphical user interface (GUI) but also logs the data to a .txt file for further analysis or record-keeping.

**Step-by-Step Procedure:**
  1.	Connect the DHT11/DHT22 Sensor to the Arduino:
    o	Follow the wiring diagram as per attached image (Arduino-DHT11-Connections).
    o	Typically, you would connect the sensor’s VCC to the Arduino's 5V pin, GND to GND, and the data pin to one of the digital pins, e.g., Digital Pin 2.
  2.	Connect the Arduino to the Computer:
    o	Use a USB cable to connect the Arduino Uno to your computer.
  3.	Upload the Arduino Sketch:
    o	Open the Arduino IDE and load the sketch named "Humidity_and_Temp_SENSOR". This sketch was originally written by ladyada and is available in the public domain.
    o	Compile and upload the sketch to your Arduino board.
    o	Note the COM port (e.g., COM3, COM4) that your Arduino is connected to. You will need to select this port in LabVIEW.
  4.	Setup LabVIEW for Data Acquisition:
    o	Open your LabVIEW program.
    o	On the front panel, locate the VISA resource name drop-down and select the COM port corresponding to your Arduino.
    o	Create a .txt file in your preferred local directory to store the acquired data.
    o	In the LabVIEW program, select the file path of this .txt file under the "Log File Path" section on the front panel.
  5.	Running the Program:
    o	Run the LabVIEW program to start acquiring and displaying the data from the Arduino.
    o	The program will continuously log the data to the selected .txt file as long as it’s running.

**Additional Considerations:**

  •	Serial Communication Configuration: Ensure that the baud rate set in the LabVIEW VISA configuration matches the baud rate in your Arduino sketch (9600).
  
  •	File Handling: Make sure the .txt file is not open in another program while LabVIEW is writing data to it to avoid access conflicts.
  
This setup allows for real-time monitoring and logging of temperature and humidity data, which can be valuable in various environmental monitoring and control applications.
