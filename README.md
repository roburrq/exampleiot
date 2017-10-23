IOT LED Example for WEMOS ESP8266

Assignment:_Set_up_basic_IoT_scenario

Requirements
Python 3.x
Running
First clone the repository to your computer via Git. Following commands are for Linux and Mac.
git clone https://github.com/roburrq/exampleiot
cd iot-led

Flashing ESP32

wget http://micropython.org/resources/firmware/esp32-20171017-v1.9.2-279-g090b6b80.bin
sudo esptool.py -p /dev/ttyUSB0 -b 460800 erase_flash
sudo esptool.py -p /dev/ttyUSB0 -b 460800 write_flash --flash_mode dio 0x1000 esp32-*.bin


On your machine
Run main.py like
python main.py
then browse to http://localhost:8080/

Run following command:
sudo ampy -p /dev/ttyUSB0 put main.py 
Troubleshooting
Resetting Device
If for any reason your device is struct, you may need to reset and reflash it.
