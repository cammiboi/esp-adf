# ESP Dispatcher DuerOS Example

This example shows how to use ADF ESP Dispatcher action APIs to connect DuerOS.

## Compatibility

| ESP32-LyraT | ESP32-LyraT-MSC |
|:-----------:|:---------------:|
| [![alt text](../../../docs/_static/esp32-lyrat-v4.2-side-small.jpg "ESP32-LyraT")](https://docs.espressif.com/projects/esp-adf/en/latest/get-started/get-started-esp32-lyrat.html) | [![alt text](../../../docs/_static/esp32-lyratd-msc-v2.2-small.jpg "ESP32-LyraTD-MSC")](https://docs.espressif.com/projects/esp-adf/en/latest/get-started/get-started-esp32-lyratd-msc.html) |
| ![alt text](../../../docs/_static/yes-button.png "Compatible") | ![alt text](../../../docs/_static/yes-button.png "Compatible") |

## Usage

Prepare the audio board:

- Connect speakers or headphones to the board.

Configure the example:

- Select compatible audio board in `menuconfig` > `Audio HAL`.
- Set up Wi-Fi connection by running `menuconfig` > `Example Configuration` and filling in `WiFi SSID` and `WiFi Password`.
- Select your DuerOS device profile instead of `ADF_PATH/components/dueros_service/duer_profile`. If you don't have a DuerOS device profile, please refer to [DuerOS Developer Certification Guide](https://dueros.baidu.com/didp/doc/overall/console-guide_markdown) and apply for a DuerOS Developer Account.

Load and run the example.


## Supported Features

- Say "Hi Lexin" to trigger the DuerOS voice interaction, green LED will turn on for indicate wakeup.
- Press [Rec] button to talk to DuerOS. The device will playback the DuerOS response. You can say anything you want, e.g."今天天气怎么样?" or "现在几点了?", which means "What's the weather today?" or " what time is it?".
- The green LED indicates Wi-Fi status:
    - Green LED on if Wi-Fi connected
    - Green LED blinks normally if Wi-Fi disconnected
    - Green LED fast blinks if Wi-Fi is under setting
- Adjust volume via [Vol-] or [Vol+]
- Configure Wi-Fi by [Set] button

### Note

- DuerOS profile is device unique ID.
- DuerOS support Chinese language only.
- There is a specific configuration for DuerOS example, please refer to [sdkconfig.defaults](sdkconfig.defaults).
