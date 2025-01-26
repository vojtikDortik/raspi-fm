
Raspi-FM
=========

Raspi-FM is a lightweight and user-friendly FM transmitter project based on the [fm_transmitter](https://github.com/markondej/fm_transmitter) app made by [markondej](https://github.com/markondej/) that makes it possible to broadcast FM audio signal.
<p align="center">
 <img src="https://raw.githubusercontent.com/vojtikDortik/raspi-fm/refs/heads/main/images/webapp.png" style="width: 50%; height: auto;">
</p>

Features
--------
1. **Web Interface**: Control the FM transmitter via a browser by connecting to the Wi-Fi AP and accessing `http://192.168.4.1:5000`.
2. **Audio Playback**: Select audio files to play on the FM transmitter.
3. **Custom Frequency**: Set the desired FM frequency for broadcasting.
4. **Predefined Stations**: Choose from a list of all Prague FM stations (I want to add custom stations list option)

Installation
------------
To install raspi-fm, just run this on your Raspberry Pi:
```bash
curl -fsSL https://raw.githubusercontent.com/vojtikDortik/raspi-fm/refs/heads/main/install.sh | sudo bash
```
I tested this only on my Raspberry Pi Zero W, but I will test it on other Pi's too.


Supported devices
-----------------
As I said before, I tested this only on my Pi Zero W, but it should work on most Pi's with WiFi except Pi 5 and 4.


Usage
-----
After successful installation, the Pi should start a WiFi access point named `raspi-fm`, that you can connect to using `flipfmsignal` password. Then you can open your web browser and open it's default IP with port 5000 `http://192.168.4.1:5000`. If you have problems conneting to the AP, try turning off your data connection (if you are on a phone) and disable autoconnect to known nearby WiFi's.







To-Do
-------

- [ ] Bash installer script
- [ ] Broadcast start timer
- [ ] Custom stations list
- [ ] Phone bluetooth audio stream (this will be hard)
- [ ] Existing audio files managment (renaming, deleting)




### Systemd Services
- `raspifm-app.service`: Manages the Flask web app.
- `raspifm-wifi.service`: Handles the Wi-Fi access point setup.

### Adding Audio Files
Place your audio files in the `audio_files/` directory located in the project folder. You can also upload it using the web UI.




## License
[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-nd/4.0/)
This project is licensed under the [Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International License](https://creativecommons.org/licenses/by-nc-nd/4.0/). 

You are free to:
- **Share** — copy and redistribute the material in any medium or format.

Under the following terms:
- **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made.
- **NonCommercial** — You may not use the material for commercial purposes.
- **NoDerivatives** — If you remix, transform, or build upon the material, you may not distribute the modified material.


