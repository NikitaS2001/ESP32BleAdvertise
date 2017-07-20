# ESP32ArduinoBeacon
Simple library of a BLE advertise using ESP32 in Arduino

### Usage
```
void setup() {
    Serial.begin(115200);
    ble.begin("3ab87438");  //sets the device name
}

void loop() {
    String str = String(random(0, 1000));
    ble.advertise(str);   // advertises a random number
    delay(1000);
}
```

### Downloading and Installing
Click on the green button "Clone or download" and download as a zip file.
In Arduino Studio, click in `Sketch > Include Library > Add .ZIP Library` and select the file you've just downloaded.

### Tips
Be aware of the limitations of the BLE broadcast in terms of the message size. Roughly, your message and device name combined should not be bigger than 20 bytes.