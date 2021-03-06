# MicroPython envirobit:bit library for the BBC micro:bit

# Installing

enviro:bit consists of:

* a tcs3472 colour sensor, 
* a bme280 temperature, pressure and humidity sensor
* a mems microphone

Files are supplied for each of these features, and you can pick and choose what to use in your project.

Copy the driver files from you need from the library/ folder into your "mu_code" folder, this might be in:

* C:\Users\YourUserName\mu_code on Windows
* /Users/YourUserName/mu_code on macOS

Create a new blank file in Mu for your project, leave it blank and Flash it to your micro:bit with the Flash button. You can close this for now.

Create another new file, save this one as "main.py" and keep it open.

Now open the "Files" dialog (you might have to close the "Repl" first) and drag and drop main.py and the driver .py files from the right pane, to the left pane.

When you reset your micro:bit, it will load main.py- so you can "import" the libraries and start writing your code here!

# Function Reference

## bme280

For temperature, pressure and humidity readings you must use the bme280 driver. First initialise it like so:

```
import bme280
bme = bme280.bme280
```

Your class instance, `bme`, will now have the following methods:

* `bme.temperature()` - return the temperature in degrees C
* `bme.pressure()` - return the pressure in hectopascals
* `bme.humidity()` - return the relative humidity in %
* `bme.altitude()` - return the altitude in feet, calculated against the current QNH value
* `bme.set_qnh(value)` - set the QNH value for calculating altitude

