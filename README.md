# WifiEivilTwin
WiFi Deauther + Evil-Twin Tool using ESP8266

This project uses an ESP8266 to perform WiFi attacks such as Deauthentication and Evil-Twin AP spoofing. It can run both attacks simultaneously without needing to toggle either mode.
🚀 Features

    Deauth Attack: Disconnects clients from a selected WiFi access point.

    Evil-Twin Attack: Creates a fake AP to capture WiFi passwords with real-time verification against the original AP.

    Simultaneous Attacks: Both Deauth and Evil-Twin can run concurrently.

⚠️ DISCLAIMER

    This code is provided for educational purposes only. You are solely responsible for how you use it. Only use it on your own networks and devices.
    Check and comply with your country's laws before using this tool.

🛠 Installation (Arduino IDE)

    Install Arduino IDE.

    Go to File → Preferences and add this URL to the "Additional Boards Manager URLs":

    https://raw.githubusercontent.com/SpacehuhnTech/arduino/main/package_spacehuhn_index.json

    Go to Tools → Board → Boards Manager, search for and install the Deauther package.

    Download and open the PhiSiFi project with Arduino IDE.

    Under Tools → Board, select an ESP8266 Deauther board.

    Connect your ESP8266 and select the correct COM port under Tools → Port.

    Click Upload.

📲 How to Use

    Connect to the AP:
    SSID: b4dcyber
    Password: 12345678@

    In your browser, select the target AP to attack.
    (AP list refreshes every 30 seconds – reload page to update)

    Click:

        Start Deauthing to begin disconnecting clients.

        Start Evil-Twin to spoof the selected AP.

    Reconnect to the spoofed open network (same SSID as the target).

    To stop any attack:

        Visit 192.168.4.1/admin while connected to the fake AP.

        Or simply reset the ESP8266.

    When a correct password is captured, you'll see a message:

    Successfully got password for - TARGET_SSID - PASSWORD

    Note: If the device loses power or is reset, all gathered info will be lost.

🧩 Troubleshooting

    “It doesn’t work for me.”

    This was built as a fun side project and proof-of-concept. No official support is provided.

    For in-depth info on why deauth attacks might fail, read Spacehuhn’s blog:
    https://blog.spacehuhn.com/deauth-attack-not-working

    If you have constructive feedback or find a bug, feel free to report it — no promises, but I might fix it when I have time.

Would you like this turned into a README.md file or packaged for GitHub?
You said:
can you create a epstool.py read me file
ChatGPT said:

Certainly! Below is a professional and clearly formatted README.md file for a hypothetical epstool.py script — assuming it’s part of your ESP8266 WiFi Deauther + Evil-Twin tool project.

If epstool.py has a different purpose or specific CLI/API behavior, let me know, and I’ll tailor the file accordingly.

# epstool.py

`epstool.py` is a utility script designed to assist with managing and deploying the ESP8266-based WiFi Deauther + Evil-Twin tool. It helps automate flashing, configuration, and data extraction tasks when working with the ESP8266 board.

---

## 🔧 Features

- Flash compiled firmware to an ESP8266 device
- Extract stored password data from the device (if any)
- Reset the device to default settings
- Provide serial interface for debugging/log monitoring

---

## 🚀 Requirements

- Python 3.7+
- `pyserial`
- `esptool` (for flashing ESP8266 firmware)
- Admin/root privileges (optional, depending on OS for serial access)

### Install dependencies:

```bash
pip install pyserial esptool

🛠 Usage

python epstool.py [command] [options]

Commands:
Command	Description
flash	Flash firmware to the ESP8266 board
read	Read output from the device via serial console
reset	Reset ESP8266 (reboots and wipes temp data)
get-passwords	Attempt to extract captured credentials (if supported)
📦 Example Usage
Flash firmware:

python epstool.py flash --port COM3 --baud 115200 --bin firmware.bin

Read serial output:

python epstool.py read --port /dev/ttyUSB0 --baud 74880

Reset device:

python epstool.py reset --port COM3

⚠️ Legal Disclaimer

This tool is provided strictly for educational and research purposes. Use it only on networks and devices you own or have explicit permission to test.

    Unauthorized access to networks is illegal and unethical.
    Always follow applicable laws and guidelines in your region.

📚 Related Resources

    ESP8266 Deauther Project (Spacehuhn)

    Arduino IDE Installation Guide

    Spacehuhn Blog on WiFi Deauth

💬 Support

This script is maintained for personal use and experimentation. While issues and suggestions are welcome, no official support is provided.


---

Let me know if you'd like this turned into a real `epstool.py` implementation or if the script already exists and you want the README tailored to its exact functions.

