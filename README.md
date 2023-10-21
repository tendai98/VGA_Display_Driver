## ESP32 VGA Text-Display

This project showcases how to use an ESP32 to drive a VGA monitor for displaying text sent over a Wi-Fi connection. The ESP32 is set up as a web server, allowing users to transmit text messages for display on the VGA monitor. The project is structured into different components, each serving a specific purpose.

### Project Structure

- `hardware.h`: Initializes and manages hardware components, such as LEDs and a buzzer.
- `http.h`: Sets up a web server, handles HTTP requests for message display, and manages system functions.
- `vga.h`: Manages the VGA display and defines the introductory text to be displayed.
- `wifi.h`: Configures the ESP32 as a Wi-Fi access point for communication.

### `hardware.h`

This module contains functions for initializing and controlling various hardware components:

- `initHardware()`: Initializes hardware components like LED and a buzzer.
- `driveAlert()`: Activates LEDs and buzzer for alert notifications.

### `http.h`

This component sets up a web server and handles incoming HTTP requests for different functionalities:

- `/push`: Handles requests to display a text message on the VGA monitor.
- `/clear`: Manages requests to clear the screen on the VGA monitor.
- `/alert`: Handles alert-related actions like activating LEDs and the buzzer.
- `/reset`: Manages system reset requests.
- `/auth`: Handles user authentication.
- `/pin`: Manages security PIN settings.
- `/lock`: Handles requests to lock/unlock access to the display.

### `vga.h`

This module manages the VGA display and includes introductory text:

- `initVGA()`: Initializes the VGA display with the appropriate settings.
- `vgaPrintBuff()`: Displays text on the VGA monitor.
- `vgaPrintLine()`: Inserts a line break.
- `vgaClear()`: Clears the VGA display and shows an introductory banner.

### `wifi.h`

This module is responsible for configuring the ESP32 as a Wi-Fi access point:

- `initWiFiAP()`: Sets up the ESP32 as a Wi-Fi access point with the specified name and password.
