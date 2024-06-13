#ESP32 MPU6050 Bluetooth Communication with OpenGL Visualization

This project demonstrates how to read accelerometer data from an MPU6050 sensor connected to an ESP32 and transmit this data via Bluetooth to a Python script. The Python script uses PySerial to read the data and OpenGL (via PyOpenGL and Pygame) to visualize the sensor readings in real-time.

## Components

1. **ESP32**: Microcontroller with built-in Bluetooth.
2. **MPU6050**: 6-axis MotionTracking device that combines a 3-axis gyroscope and a 3-axis accelerometer.
3. **Python Script**: Receives data via Bluetooth and visualizes it using OpenGL.

## Prerequisites

- ESP32 Development Board
- MPU6050 Sensor
- Bluetooth-enabled Computer
- Python 3.x
- Required Python libraries: `PySerial`, `PyOpenGL`, `Pygame`

## Hardware Setup

1. Connect the MPU6050 to the ESP32:
    - VCC to 3.3V
    - GND to GND
    - SCL to GPIO 22
    - SDA to GPIO 21

## Software Setup

### 1. ESP32 Code

Upload the appropriate code to your ESP32. This code initializes the MPU6050 sensor and sets up Bluetooth communication to transmit accelerometer data.

### 2. Python Script

1. Install the required Python libraries:

    ```sh
    pip install pyserial PyOpenGL pygame
    ```

2. Save and run the provided Python script. This script connects to the ESP32 over Bluetooth, reads the sensor data, and visualizes it using OpenGL.

## Usage

1. **Pair the ESP32 with Your Computer**:
    - Ensure that your ESP32 is discoverable and pair it with your computer.
    - Note the COM port assigned to the ESP32 Bluetooth connection (e.g., COM27).

2. **Replace the COM Port in the Python Script**:
    - Update the COM port in the `serial.Serial` initialization with the actual COM port of your ESP32.

3. **Run the Python Script**:
    - Execute the Python script to start receiving and visualizing data from the ESP32.

## Notes

- Ensure the data format from the ESP32 matches the expected format in the Python script: `ax,ay,az`.
- Adjust the baud rate and COM port settings as necessary to match your hardware configuration.

## Troubleshooting

- **Serial Connection Issues**: Ensure the correct COM port is used and the ESP32 is properly paired with your computer.
- **Data Parsing Errors**: Verify the data format being sent from the ESP32 matches the expected format in the Python script.
- **OpenGL Visualization Problems**: Ensure your system supports OpenGL and you have the required libraries installed.

## License

This project is licensed under the MIT License. 
