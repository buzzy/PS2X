PS2X
====
PS2 controller library for ESP8266

====
PS2X pad;

setup():
pad.ConfigGamepad(DAT_PIN, CMD_PIN, ATT_PIN, CLK_PIN, true, true);

loop():
//set the second parameter to 255 to make the motor rumble
pad.ReadGamepad(false, 0);

//Possible button values are found in the .h file
Serial.print(pad.Analog(ANALOG_BUTTON_TO_READ));
Serial.print(pad.Button(DIGITAL_BUTTON_TO_READ));
