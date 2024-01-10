# Attendance
System for maintaining a database of employee arrival and leaving times in multiple work settings.

![image](https://github.com/mopac/attendance/assets/5881829/6f57c495-e3ed-42e0-981c-5209a19f214e)
![20240103_161211](https://github.com/mopac/attendance/assets/5881829/143f39f9-79a5-453e-90c1-a024b3d0af73)

The system uses remote boxes that respond to fingerprints or tags to identify the employee. That remote box must be connected to wifi, and it makes a web request to a central server that logs the check-in/check-out times.
The central server is managed via a web interface.
Any number of remote boxes can be added and all will access the same central server.

## Remote Box
The remote box is based on ESP32 COW board. 
Connected to the ESP32 are:
- 128 x 64 monochrome OLED display connected via I2C
- RC522 Tag reader connected via SPI
- Fingerprint scanner connected via UART
- Piezo Electric Buzzer

The box is powered by an external 5V power supply.
All the components are powered from the 3.3V regulator on ESP32
Below is the schematic that shows how they are all connected


![image](https://github.com/mopac/attendance/assets/5881829/67f875c4-a06f-4ec3-a245-98931889153f)

