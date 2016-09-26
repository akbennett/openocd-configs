# openocd configs
- stlink-v2.1-nrf51.cfg - st-link v2.1 + nrf51
- stlink-v2-nrf51.cfg - st-link v2 + nrf51  (Qunqi Mini ST-link/V2 programmer)
- stlink-v2-stm32f4x.cfg - st-link v2 + stm32f4 (Linaro Carbon board)

### Dependencies
- install openocd (apt-get install openocd)
or
```
apt install pkg-config automake libtool
git clone git://git.code.sf.net/p/openocd/code openocd-code
cd openocd-code
./bootstrap
./configure
make
make install
```
### Execute openocd
```
openocd -f [configfilename.cfg]
```
### Program a device directly using openocd command line
```
openocd -f stlink-v2-stm32f4x.cfg -c "program zephyr.hex verify exit"
```

### Connect to openocd and program device
```
telnet localhost 4444
program /path/to/hexfile.hex
```
