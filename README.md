# ESP32-VL53L0X

VL53L0X library
- Platform: ESP-IDF (e.g. ESP32)
- See include file for details of functions

Copyright © 2019 Adrian Kennard, Andrews & Arnold Ltd, and original authors. See LICENCE file for details. GPL 3.0

### 2025/04/07 - Luong Huu Phuc ###
***Fix bug can not install I2C***
Change from (**revk** repo):
```c
  if (vl53l0x_i2cFail(v))
    return "I2C fail";

  return NULL;
```
to: 
```c
  if (vl53l0x_i2cFail(v) == 0)
    return "I2C fail";

  return NULL;
```
