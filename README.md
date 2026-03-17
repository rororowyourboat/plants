# Plants

Plant monitoring system using a UNIHIKER M10 single-board computer.

## Hardware

- **Board:** UNIHIKER M10 (DFRobot DFR0706)
- **CPU:** RK3308 quad-core Cortex-A35 @ 1.2GHz
- **Co-processor:** GD32VF103 RISC-V (handles GPIO/sensors)
- **RAM:** 512MB DDR3
- **Storage:** 16GB eMMC (~8.4GB free)
- **Display:** 2.8" touchscreen, 240x320
- **OS:** Debian 10, Python 3.7.3
- **Wireless:** WiFi 2.4G + Bluetooth 4.0
- **Built-in sensors:** Light, accelerometer, gyroscope, microphone, buzzer

## Network Setup

The UNIHIKER connects to a local 2.4G WiFi network with a static IP configured via NetworkManager. SSH access uses key-based auth with a dedicated key and an alias (`ssh uh`) in `~/.ssh/config`.

The board can be powered from any 5V USB-C source and will automatically connect to WiFi on boot.

## Python Libraries (pre-installed on UNIHIKER)

- **UNIHIKER library** -- screen display, graphics, audio, input control, threading
- **PinPong library** -- GPIO, onboard sensors, I2C/UART/SPI, servo, LED strips, DHT11, ultrasonic
- NumPy, Matplotlib, Pandas, TensorFlow, Jupyter

## Quick Start

```bash
# SSH into the UNIHIKER
ssh uh

# Run a Python script
python3 main.py
```

## Roadmap

- [ ] **Hello World** -- display text on the touchscreen, blink the LED
- [ ] **Read onboard sensors** -- light, accelerometer, gyroscope via PinPong
- [ ] **Plant moisture monitoring** -- analog soil moisture sensor + screen display
- [ ] **Temperature & humidity** -- DHT11 sensor logging
- [ ] **IoT dashboard** -- push sensor data to SIoT/MQTT, view remotely
- [ ] **Voice recognition** -- use built-in microphone for voice commands
- [ ] **Speech synthesis** -- text-to-speech feedback on plant status
- [ ] **AI voice assistant** -- integrate with OpenAI API for natural language plant care Q&A
- [ ] **Automated alerts** -- notifications when soil is dry or conditions change
- [ ] **Camera integration** -- USB camera for plant health visual monitoring

## Resources

- [UNIHIKER Wiki](https://www.unihiker.com/wiki/)
- [PinPong Library Docs](https://www.unihiker.com/wiki/LanguageReference/PinPong_Library/)
- [DFRobot Product Page](https://www.dfrobot.com/product-2691.html)
