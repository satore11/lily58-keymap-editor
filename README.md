# My Custom Lily58 ZMK Firmware  teclado

Welcome to my personal ZMK firmware configuration for the Lily58 split keyboard! This setup is tailored for a wireless experience with Nice!Nano v2 controllers.

## ⌨️ Key Features

*   **Wireless & Split:** Designed for a clean, wireless desk setup.
*   **OLED Display:** Shows current layer and keyboard status.
*   **Multiple Layers:** Access to symbols, numbers, and function keys without leaving the home row.
*   **VIM-style Navigation:** Arrow keys on the home row for efficient coding and text editing.

## 🗺️ Keymap

This configuration uses a custom keymap focused on productivity and comfort. Here is a quick look at the layout:

![Keymap Layout](./my_keymap.png)

*   **Base Layer:** Standard QWERTY layout.
*   **Lower Layer:** Access to numbers, function keys, and Bluetooth controls.
*   **Raise Layer:** VIM-style navigation and special characters.

## 🚀 Getting Started

The easiest way to use this firmware is to grab the latest build from the **Actions** tab in this repository.

1.  Go to the [**Actions** page](https://github.com/s-orlando/zmk-config/actions).
2.  Click on the latest successful workflow run.
3.  Download the `firmware` artifact.
4.  Follow the standard ZMK instructions to flash the `.uf2` files to your Nice!Nano controllers.

## 🛠️ Customization

Feel free to fork this repository and customize the keymap to your liking! The main configuration files are:

*   `config/lily58.keymap`: The heart of the keymap. Edit this to change key bindings.
*   `config/lily58.conf`: Hardware-specific settings (e.g., enabling OLEDs).

## 👨‍💻 Building Locally

If you prefer to build the firmware yourself, you can use `west` (the Zephyr meta-tool).

```bash
# Build the firmware for both sides
west build -p auto -b nice_nano_v2 -- -DSHIELD="lily58_left lily58_right"
```

This will create the `.uf2` files in the `firmware` directory.