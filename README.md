# dualsense-haptics

A single-file, zero-dependency **Sony DualSense** (and DualSense Edge) haptic & rumble synthesizer built on **WebHID**.

Open the HTML file in Chrome or Edge, connect your controller, and feel real-time synthesized textures, manual dual-actuator sliders, and analog trigger-to-rumble feedback.

## Live Demo

Open this link (hosted on GitHub Pages): [Click me!](https://semen1207.github.io/dualsense-haptics/)

**Browser support:** WebHID is required. Chrome or Edge on desktop only (close background apps like Steam Input or DS4Windows first).

## Features

| Feature | Status |
| :--- | :---: |
| **Dual-Actuator Sliders** (Independent Left Heavy & Right Crisp motors) | ✅ |
| **Trigger-to-Rumble** (Squeeze L2 / R2 for live proportional vibration) | ✅ |
| **6 Synthesized Textures** (Heartbeat, V8 Engine, Raindrops, Chainsaw, Ocean Wave, Rapid Recoil) | ✅ |
| **Live Dual-Channel Oscilloscope** (Real-time Left/Right waveform plot) | ✅ |
| **Reactive Lightbar** (LED color shifts dynamically with vibration intensity) | ✅ |
| **USB + Bluetooth Auto-Detection** (Report `0x02` vs `0x31` + CRC32) | ✅ |

## How It Works

* **60Hz Haptic Engine:** Synthesizes custom vibration waveforms and sends Left/Right actuator bytes (`0–255`) at 60Hz alongside dynamic RGB lightbar updates.
* **USB vs. Bluetooth:** Automatically detects connection type from input report length (`63B` USB vs `77B` Bluetooth) and signs Bluetooth `0x31` output packets with a `0xA2`-prefixed CRC32 checksum.

## License

MIT
