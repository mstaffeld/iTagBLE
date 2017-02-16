# iTagBLE

## A cheap bluetooth button called iTag. 

1. Press the button for 3 seconds, you will hear a long beep. 
2. Scan for the button mac address 
3. run gatttool, connect, primary, char-desc

```
sudo hcitool lescan | grep iTag
sudo gatttool -b FF:FF:30:00:04:76 -I
connect
primary
char-desc
```

When you press the button you will see the following gatttool output:
```
Notification handle = 0x000e value: 01 
```

There are tools in python that will allow you to connect to gatttool and write code against the bluetooth button press received event. 

# notes
-iTag button
[Link to Amazon](https://www.amazon.com/Anti-Lost-Bluetooth-Remote-Shutter-Tracker/dp/B00WB4EPKO)


- http://flowcloud.github.io/ci20-bluetooth-LE/2015/09/10/bluetooth-control-in-python/
- https://github.com/peplin/pygatt