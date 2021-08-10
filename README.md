# WebDAQ Ubuntu 18.04 64-bit DAQ driver

## DAQ Library and Driver Installation

1. Connect an Ethernet cable to the WebDAQ and verify that you have a working connection to the internet.

2. Update your package list:

``` sh
  sudo apt-get update
```

3. Download the DAQ driver:

```sh
  cd ~
  wget https://github.com/sbazaz/webdaq_ubuntu/raw/main/libulwd-ubuntu18-x64.0.0.1.b4.tar.bz2
```

4. Extract and install the driver:

``` sh
  tar -xvjf libulwd-ubuntu18-x64.0.0.1.b4.tar.bz2
```

5. Run the following commands to install the library:

``` sh
  cd libulwd
  sudo sh install.sh
```

6. Reboot the WebDAQ system

### Examples

#### Python
The Python examples are located in the examples folder. To execute the examples, run the following commands:

``` sh
  cd ~/libulwd/examples/python
  ./a_in_scan.py
  ./a_in_scan_iepe.py
```

#### C
The C examples are located in the examples folder. Run the following commands to build the examples:

``` sh
  cd ~/libulwd/examples/c
  make
```

To execute the examples, run the following commands:

``` sh
  ./AInScan
  ./AInScan_IEPE
```

### Documentation
Online Python help for the DAQ library is available at https://nwright-mcc.github.io/webdaq_raspbian/.

#### Note: The DAQ module's firmware is stored in a volatile memory, therefore the firmware image will be lost when the WebDAQ system is shut down. The ulGetDeviceInventory function loads the firmware image to the module when it is invoked for the first time after system boot up. Loading the firmware image takes about 5 to 8 seconds.


