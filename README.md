# D1MiniDev-S3DP
## Syracuse 3D Printing D1 Mini Dev Board Resources

### In this repository:
- Technical Specifications & Instructions
- STL Models of Enclosure
- STEP Model of PCB w/Electronics to make your own enclosure
- Sample ESPHome Configuration
- Sample Home Assistant Automation for LED

### Available for purchase here as a bare PCB or fully assembled:
[https://syracuse3dprinting.com/product-category/smart-home/](https://syracuse3dprinting.com/product-category/smart-home/)

The D1MiniDev, designed by Syracuse3DPrinting, is a compact and versatile device ideal for DIY enthusiasts. Utilizing the well-regarded D1Mini ESP8266 microcontroller, this device provides a range of inputs and outputs suitable for a myriad of applications.

### Key Features:

**MAX6675 + K Type Thermocouple**: The device integrates a MAX6675 thermocouple amplifier and a K type thermocouple, which offer precise temperature measurements. This functionality is crucial for projects requiring temperature monitoring, including HVAC diagnostics.

**WS2812B RGB LED**: The D1MiniDev contains a programmable WS2812B RGB LED, which can be customized to change colors based on varying conditions, including temperature fluctuations.

**2x Momentary Push Buttons**: These buttons serve as binary inputs for Home Assistant, enabling users to control various aspects of their smart home system, such as adjusting lighting or activating scenes, directly from the device.

**Power Regulator with 7-28VDC and USB Input**: The D1MiniDev is designed with flexibility in mind, with a power regulator compatible with a wide array of power sources, ranging from 7 to 28VDC and including USB power.

**Dual 6 Pin Molex Minifit Connectors**: The D1MiniDev is equipped with dual 6 pin Molex minifit connectors, facilitating connectivity with other devices or modules and allowing for potential expansion of its functionality.

**ESPHome Configuration**: A sample ESPHome configuration for the D1MiniDev is available for download, ensuring a smooth integration process with the Home Assistant platform.

Users can choose between three different formats for the D1MiniDev: a bare PCB for those interested in a completely hands-on assembly experience; a DIY Kit that includes the PCB and components of your choice; or a fully assembled unit for immediate use. An optional 3D printed enclosure, purchasable or self-printable for those with a 3D printer, is available for added device protection.

### Technical Specifications: D1MiniDev by Syracuse3DPrinting

**Microcontroller**
- D1Mini ESP8266

**Temperature Measurement**
- MAX6675 Thermocouple Amplifier
- K Type Thermocouple

**Visual Indicator**
- WS2812B RGB LED (Programmable)

**User Inputs**
- 2x Momentary Push Buttons (Home Assistant Compatible)
- 3x Digital I/Os via 6-Pin Molex Headers
- 1x Analog I/O via 6-Pin Molex Headers

**Power Options**
- Power Regulator: 7-28VDC Input, 500mA
  - Optional onboard PTC Fuse is limited to 16VDC in
- USB Power Input - 5V via USB on D1 Mini
- Daisy Chain ability - When powered with 12V, Use 6-Pin headers to provide power from one board to another.
  - Recommended to bypass onboard fuse and use external fusing on the power supply for daisy chain applications

**Connectivity**
- Dual 6 Pin Molex Minifit Connectors (For Daisy Chaining and Expandability)
- Smart Home via Wifi (2.4ghz) - Designed for ESPHome via Home Assistant
  - Includes Sample ESPHome Configuration for Home Assistant Integration

**Form Factor Options**
- Bare PCB
- DIY Kit with PCB and Selected Components
- Fully Assembled Device

**Additional Accessories**
- Optional 3D Printed Enclosure (Purchasable or DIY Print)
- Please note that the final assembled size of the device will depend on the chosen components and the use of the optional enclosure.


## Bill of Materials

Most parts are optional based on configuration.

| Component | Specs | Part Number | Link |
| --- | --- | --- | --- |
| DC-DC Converter | 7-28VDCin 5VDC Out 500mA | R-78E5.0-0.5 | [DigiKey](https://www.digikey.com/en/products/detail/recom-power/R-78E5-0-0-5/2834904) |
| Power Supply Filtering Capacitors x2 | 10UF 10V X7R 0805 | CL21B106KPQNNNG | [DigiKey](https://www.digikey.com/en/products/detail/samsung-electro-mechanics/CL21B106KPQNNNG/3894474) |
| Push Button Tactile Switch x2 | - | B3F-4055 | [DigiKey](https://www.digikey.com/en/products/detail/omron-electronics-inc-emc-div/B3F-4055/31799) |
| PTC Resettable Fuse | 750 mA 16V | 0ZCJ0075AF2E | [DigiKey](https://www.digikey.com/en/products/detail/bel-fuse-inc/0ZCJ0075AF2E/4156135) |
| RGB Addressable LED | WS2812B | COM-16347 | [DigiKey](https://www.digikey.com/en/products/detail/sparkfun-electronics/COM-16347/11630204) |
| 6-Pin Molex MiniFit Header | - | 0353180620 | [DigiKey](https://www.digikey.com/en/products/detail/molex/0353180620/3185064) |
| 12V Power Input (5.5x2.1MM Barrel Jack) | - | CON-SOCJ-2155 | [Mouser](https://www.mouser.com/ProductDetail/Gravitech/CON-SOCJ-2155?qs=fkzBJ5HM%252BdCcpvFQyQZHtA%3D%3D) |
| D1 Mini ESP8266 | - | - | [Amazon](https://amzn.to/3rinfvB) |
| MAX6675 Module + K Type Thermocouple | 3-5V M6 | - | [Amazon](https://amzn.to/3rlv4Av) |

## Issues/Limitations

- The silkscreen outline of the ESP8266 is mirrored on v1.0 of the PCB. When assembling follow the assembly pictures instead of using the silkscreen outline for this component.
- The onboard PTC Fuse is limited to 16V. If using a 24VDC power supply it's recommended to bypass this fuse and use an external fuse.