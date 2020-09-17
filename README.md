# picoCore (pcfreak1201)
Small Arduino/Wiring core for 8-pin tiny AVRs: ATtiny85 series.  Arduino Blink sketch compiled for the ATtiny85 is 64 bytes. Goal (pcfreak1201): bare ATtiny85 core with serial support, but no bootloader (for fast startup without delay).

nerdralph writes this core from scratch, with code size and efficiency as the main goal.  He is making use of AVR assembler code when the code size and efficiency goals cannot be readily attained with C/C++.  Unlike the official AVR core, picoCore has compile-time checking of many arguments.  Calling digitalWrite(42) will cause a compile error with the message, "pin out of range". 

## Development Status
v0.3.1 replacement of [debugSerial](https://github.com/nerdralph/debugSerial) by [picoUART] (https://github.com/pcfreak1201/picoUART)
v0.3.0 includes [debugSerial](https://github.com/nerdralph/debugSerial), for basic serial output supporting the most common [Serial.print()](https://www.arduino.cc/reference/en/language/functions/communication/serial/print) data types.

## Supported Functions
* [analogRead()](https://www.arduino.cc/en/Reference/AnalogRead)
* [analogReference()](https://www.arduino.cc/en/Reference/AnalogReference)
* [analogWrite()](https://www.arduino.cc/en/Reference/AnalogWrite)
* [delay()](https://www.arduino.cc/en/Reference/Delay)
* [delayMicroseconds()](https://www.arduino.cc/en/Reference/DelayMicroseconds)   *wrapper for _delay_us()*
* [digitalRead()](https://www.arduino.cc/en/Reference/DigitalRead)
* [digitalWrite()](https://www.arduino.cc/en/Reference/DigitalWrite)
* [millis()](https://www.arduino.cc/en/Reference/Millis)   *Watchdog timer based. Will increase with steps of 16*
* [pinMode()](https://www.arduino.cc/en/Reference/PinMode)
* [shiftIn()](https://www.arduino.cc/en/Reference/ShiftIn)
* [shiftOut()](https://www.arduino.cc/en/Reference/ShiftOut)

