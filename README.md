## README

# Risk detection and alert system

This stm32-based project monitors various environmental conditions using multiple sensors and alerts the user through a buzzer and an LED when certain thresholds are exceeded.

## Components
- STM32F446RE
- Gas sensor (connected to A0)
- Fire sensor (connected to pin 2)
- IR sensor (connected to pin 3)
- LDR sensor (connected to A1)
- DHT22 sensor (connected to pin 4)
- Buzzer (connected to pin 5)
- LED (connected to pin 6)
- Connecting wires

## Pin Configuration
| Sensor/Component | Pin           |
|------------------|---------------|
| Gas Sensor       | A0            |
| Fire Sensor      | 2             |
| IR Sensor        | 3             |
| LDR Sensor       | A1            |
| DHT22 Sensor     | 4             |
| Buzzer           | 5             |
| LED              | 6             |

## Threshold Values
- **Gas Threshold**: 2
- **Fire Threshold**: LOW
- **IR Threshold**: LOW
- **LDR Threshold**: 3
- **Temperature Threshold**: 40°C
- **Humidity Threshold**: 70%

## Setup
1. Connect the sensors and components to the Arduino as per the pin configuration table.
2. Upload the provided code to the Arduino using the Arduino IDE.
3. Open the Serial Monitor at a baud rate of 9600 to see the sensor values.

## Code Explanation
The code initializes the sensors and reads their values in the `loop` function. It prints the sensor values to the Serial Monitor for debugging. If any sensor value exceeds its threshold, it activates the buzzer. The LED is controlled based on the LDR sensor's reading.

### Key Functions:
- `setup()`: Initializes serial communication, sensor pins, and the DHT22 sensor.
- `loop()`: Reads sensor values, prints them to the Serial Monitor, checks the thresholds, and controls the buzzer and LED accordingly.

## Usage
1. Ensure all sensors and components are connected properly.
2. Upload the code to the Arduino.
3. Monitor the environmental conditions through the Serial Monitor.
4. The buzzer will sound if any hazardous condition is detected, and the LED will light up based on the light intensity.

## License
This project is licensed under the MIT License. Feel free to use and modify it according to your needs.

## Contact
For any questions or suggestions, please contact [bheeshmageddapu@gmail.com].

---

By using this project, you agree to the terms and conditions of the MIT License.

## Example Output
```
Gas: 1 | LDR: 2 | Fire: 0 | IR: 1 | Temp: 25.00C | Humidity: 55.00%
Gas: 2 | LDR: 3 | Fire: 1 | IR: 0 | Temp: 26.00C | Humidity: 60.00%
Gas: 3 | LDR: 4 | Fire: 0 | IR: 1 | Temp: 27.00C | Humidity: 65.00%
...
```

This README file provides a comprehensive overview of the project, including setup instructions, pin configuration, and usage details, making it easy for users to understand and implement the system.
