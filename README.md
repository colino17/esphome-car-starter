# Remote Car Starter

## Purpose:
To integrate my dumb remote car starter with HomeAssistant. When the fob is in the proximity of my vehicle, starting the car will be possible through HomeAssistant. I used my spare fob and have it permanently placed in an inconspicuous location near where I park.

## Parts:
- D1 Mini
- Car Fob
- Three Wire Quick Connect Cables 

## Software:
- esphome
- homeassistant

## Notes:
- Similar projects seem to use resistors in various places in the wiring. I experimented with this, but found that the switch did not work with the resistors added. I suspect that the fob itself may have some sort of resistor embedded in it as the fob orignally operated using 6V battery power (two 3V batteries), but the power measured at the switch with a multimeter was considerably lower. Given that the D1 Mini provides the fob with 3V power I suspect the resistors were lowering the power rate below a certain threshold causing issues. The project seems to work well with my specific fob directly wiring the 3V power without any resistors. Whether or not this is the proper approach I am unsure. Your mileage may vary.
- I used a D1 Mini as I had a few on hand, but any ESP8266 (or even ESP32) chip should work just as well as long as you modify the project yaml appropriately.
- You may need to adjust the delay in the yaml to match the length of time you would normally hold the button on your fob.
- Additional wiring can be added to accomodate additional buttons (lock, unlock, trunk, etc). See the links below for examples.

## Useful Links:
- https://esphome.io/components/switch/gpio.html
- https://www.home-assistant.io/integrations/esphome/
- https://www.chevybolt.org/threads/ok-google-start-the-red-car.36110/
- https://gitlab.com/milagrofrost/esp8266-car-key-fob-iot/
- https://www.hackster.io/user03583/ok-google-start-my-car-7088dd
- https://hackaday.com/2017/06/04/esp8266-mqtt-remote-gate-entry/
- https://hackaday.com/2021/01/06/automating-your-car-with-a-spare-fob-and-an-esp8266/


