# PicoPlanet
![Product Image](https://github.com/bleeptrack/picoplanet/blob/master/imgs/product-img.jpg)
PicoPlanet is a series of procedurally designed PCBs.  
Available here: [Tindie](https://www.tindie.com/products/bleeptrack/picoplanet/)
More information about the design process: link coming soon  

### Features:

- Dimensions: 27.0 x 89.2 mm

- SAMD21
- USB-C
- 3 capacitive touch buttons (planets)
- 1 RGB LED
- 4 additional pins on the backside with 3.3V and 5V

### Pinout
#### Front
![Pinout Front](https://github.com/bleeptrack/picoplanet/blob/master/imgs/pinout_front.png)
#### Back
![Pinout Back](https://github.com/bleeptrack/picoplanet/blob/master/imgs/pinout_back.png)

### Usage

Important: because the PCBs are procedurally generated, the threshold values for the capacitive touch buttons might need to be adjusted by you.

#### Circuit Python (recommended)

- Download Circuit Python from [circuitpython.org](https://circuitpython.org/board/picoplanet/)
- Connect your PicoPlanet to your PC. A drive called PLANETBOOT should appear.
- Place the firmware on the PLANETBOOT drive and wait for a moment. PLANETBOOT will dismount and a new drive called CIRCUITPY will appear. 
- More information on Circuit Python can be found here: [CPY getting started](https://learn.adafruit.com/welcome-to-circuitpython)

#### Arduino
- In your Arduino IDE, unter File > Preferences add `https://boards.bleeptrack.de/package_bleeptrack_index.json` to "Additional Boards Manager URLs"
- Open your Board Manager. Search for "bleeptrack boards" and install them.
- Choose bleeptrack boards > PicoPlanet in your Board selection
- Compile and upload :)
- If Arduino does not detect your PicoPlanet board, bring your board into bootloader mode by connecting a wire to the GND pin on the backside and double tap the RESET pad with the other end of the wire. The PLANETBOOT drive should appear now and the Arduino IDE will recognize the board again 
- The LED RGB Pins can directly be accessed by `LED_R`, `LED_G`, `LED_B`

#### Troubleshooting
- `bossac` not found when compiling Arduino Sketch: reinstall `bleeptrack-boards` package or install another package that contains bossac like `Arduino SAMD Boards (32-bits ARM Cortex-M0+)`
