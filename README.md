# i2cdevlib

Forked from https://github.com/jrowberg/i2cdevlib/tree/master/Arduino/I2Cdev

See the original readme for more information

## Changes made
In I2Cdev.h, add this code around line 95, after `#ifdef` section and before class declaration:

```C++
#if defined (ESP_PLATFORM) || defined (ESP8266)
	#define min _min
	#define max _max
#endif
```
