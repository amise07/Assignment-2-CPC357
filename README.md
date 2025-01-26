# Assignment-2-CPC357  
**Soil Moisture Detection System (SMDS)**  

---

## **Summary**  
This project implements an IoT-enabled system for monitoring soil moisture levels with rain detection enhancement. The system uses sensors to measure and log soil moisture percentages and rainfall events in real time. Data is transmitted using the MQTT protocol to Google Cloud Platform (Firebase) for storage, processing, and visualization. A user-friendly dashboard offers real-time insights, and email notifications alert users when critical thresholds (e.g., low moisture levels) are detected. This system enhances water management practices, soil health monitoring, and agricultural efficiency.  

---

## **Features**  
- **Soil Moisture Monitoring**: Measure and log real-time soil moisture data.  
- **Rain Detection**: Detect and log rainfall events.  
- **MQTT Protocol**: Efficient data transmission between the ESP32 microcontroller and Google Cloud IoT Core.  
- **Real-Time Dashboard**: Interactive visualization of soil moisture and rain data on Google Cloud.  
- **Email Alerts**: Instant email notifications to users for critical conditions, such as low soil moisture.  
- **Optimized Water Management**: Supports better irrigation decisions.  

---

## **Technology Stack**  
### **Hardware**:  
- **Soil Moisture Sensor**: Measures moisture levels.  
- **Rain Sensor**: Detects rainfall.  
- **ESP32 Microcontroller**: Captures sensor data and transmits it to Google Cloud via MQTT.  
- **Wi-Fi Module**: Integrated with ESP32 for internet connectivity.  

### **Software**:  
- **Google Cloud IoT Core**: Manages device data and communication.  
- **Firebase**: For data storage and real-time dashboard development.  
- **MQTT Protocol**: Ensures reliable, lightweight data transfer.  
- **Programming Language**: C++ (Arduino IDE) for ESP32 programming.  
- **Email Library**: SMTP for Gmail-based alerts.  

---

## **Installation and Setup**  
### **Hardware Setup**:  
1. Connect the soil moisture and rain sensors to the ESP32 microcontroller as per the circuit diagram.  
2. Ensure proper power supply to the ESP32 and sensor modules.  

### **Software Setup**:  
1. **Google Cloud IoT Core**:  
   - Create a project in Google Cloud.  
   - Set up an IoT Core registry and add your ESP32 device.  
   - Generate public and private keys for device authentication.  

2. **Firebase**:  
   - Integrate Firebase into your Google Cloud project.  
   - Configure the real-time database to store sensor data.  

3. **Arduino IDE**:  
   - Install required libraries: `FirebaseESP32`, `WiFi`, `PubSubClient`, `SMTPClient`.  
   - Upload the Arduino code, which includes MQTT and sensor functionality, to the ESP32.  

4. **Email Alerts**:  
   - Set up Gmail SMTP for sending email notifications.  
   - Include recipient email addresses in the code.  

---

## **Dashboard Configuration**  
1. Develop the dashboard using HTML, CSS, and JavaScript.  
2. Fetch real-time data from Firebase and display it in graphs or tables.  
3. Deploy the dashboard on Firebase Hosting or other hosting platforms.  

---

## **MQTT Functionality**  
The MQTT protocol is used to transmit sensor data from the ESP32 microcontroller to Google Cloud IoT Core. The data includes:  
- Soil moisture percentage.  
- Rain detection status.  

The ESP32 publishes the data to the telemetry topic (`/devices/{device-id}/events`) using secure MQTT communication over TLS. Google Cloud processes this data and stores it in Firebase for visualization and alerts.  

---

## **Usage**  
1. **Data Collection**:  
   - Sensors measure soil moisture and detect rain continuously.  
   - The ESP32 sends this data to Google Cloud using MQTT.  

2. **Dashboard Visualization**:  
   - View real-time data, including graphs for moisture levels and rain events.  

3. **Email Alerts**:  
   - Users are notified via email whenever moisture levels fall below a critical threshold or when new data is uploaded.  

---

## **Contributors**  
- **Amisha Nadhira Binti Mohd Rasydan (156098)**  
- **Nabihah Asiah Binti Mohd Sukri (157651)**  

---

## **Note**  
This project is developed as part of the CPC357 assignment.  
Thank you!  
