# attocube ANC350 GUI Python
anc350_controller is a custom GUI I wrote for easy and precise control of sample position using attocube ANC350 motion controller.
This is a Python 2.7 implementation with two dependencies: `Tkinter` - for creating the GUI, and [`pyanc350`](https://github.com/Laukei/attocube-ANC350-Python-library) - which implements a python class for the C++ control functions provided by attocube (included as .dll files). The five files `anc350v2.dll`, `libusb0.dll`, `msvcp71d.dll`, `msvcr71d.dll`, and `nhconnect.dll` must be located in the same directory as `anc350_controller.py` for the GUI to run properly.

## GUI information
Here is an example showing the GUI runnig properly:

<img src = "https://github.com/ohadmich/attocube-ANC350-GUI-Python/blob/master/img/ANC350_controller.PNG" >

The upper most status bar shows the ID of the connected device, the three position boxes display the location of the sample in the x,y,z directions and the three boxes below are used for modifying the step size for each direction. The read button collects the current positions from the device and updates the position boxes. The movement control buttons move the attocubes in the desired direction by the defined step size.

The GUI can be also controlled using the keyboard for faster control. The hotkeys are defined under the `ANC350_controller` class and can be easily modified in the `__init__` function.
