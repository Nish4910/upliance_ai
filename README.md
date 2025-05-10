The simulation is done using a DHT22 sensor. Initially I had thought to use DS18B20 sensor since it has got much more temperature range which it can measure. It's range is from -55°C to +125°C, which makes it a much more efficient sensor but the major problem which i faced during wokwi simulation is that i couldn't use real time analysis for measuring the temperatures. The only option was to change the values of temperature from diagram.json in wokwi which didn't match my code's algorithm.

There are 2 codes present here, one with nRF BLE the other is wokwi's simulation code. Wokwi doesn't simualte BLE or nRF Connect App so i had to use 2 different codes.

The sensor identifies the data fetched by DHT22 Sensor and then it's reposible to send alerts to nRF Connect and also display it at the serial monitor. There are pre defined conditions such as 
idle == 0-10 deg,
heating == 10-55 deg,
stabilizing == 55-65,
target reached == 65-75,
overheat == 75-80.

This completes my simulation of a basic heater. To simulate turn on and off situations I have used a buzzer and led.
