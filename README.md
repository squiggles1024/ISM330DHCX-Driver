# ISM330DHCX

Simple ISM330DHCX Accelerometer and Gyroscope Sensor Driver

To use, include .c and .h files in your project.

The user must:

1. Create a ISM330DHCX_Handle_t instance.
2. Create a ISM330DHCX_InitSettings_t struct with the desired device settings. It is recommended the user reference the data sheet for setting details.
3. Provide a Low Level IO Driver structure "ISM330DHCX_IO_t". At a minimum, this must include a "Read", "Write", and "GetTick" function. Unused function pointers should be set to NULL. If the user does not provide an IO Init function, the GPIO and communication bus must be initialized already.
4. Pass the created ISM330DHCX_Handle_t instance, ISM330DHCX_InitSettings_t instance, and ISM330DHCX_IO_t instance to the function "ISM330DHCX_Init" function.

Note that this driver does not include functionality for many of the 'embedded' and 'sensor hub' functions.
