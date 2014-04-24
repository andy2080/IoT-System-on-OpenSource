#How to Use IoT System--Based on the OpenSource Hardware
===================

IoT (Internet of Things) system is one of Wireless Sensor Sytems (WSN). Based on the open source hardware, like Arduino, Raspberry pi, Beaglebone, and so on, anyone can conveniently buit up his own IoT system by using such WSN platform, and aslo would like to present [some demos](http://blog.smartarduino.com/) based on this platform

##User Guidance 

Step One: [Get API Key] (http://www.iot.fm/ext/examples/desktop/desktop.php), which will be used in the control protocol; 

Step Two: Add sensor nodes, such as smoke, temperature,gas.

Step Three: Design nodes control protocol. By this protocol, we can control the sensed information (e.g., temperature, or gas), please see the [protocol degsin](##Protocol Design).

Step Four: Data Dsiplay. In this step, you can use simple clicks to see the results exhibition, which are shown intuitively by pie figure.

##Protocol Design

In such WSN system, the control protocol is very important. In our protocol degsin, we have designed two types of control protocols presented by the followings.

* Upload Protocol
  * Using HTTP protocol including the following steps
    1) Using GET method;
    2) Request URL: http://api.iot.fm/upload.php,
         Parameters: uid=user name (the default name is demo); 
                     id&key=secret key generated by the step one in User Guidance [##User Guidance]
                     &sensor_name=sensor1&data=37&sensor_name=sensor2&data=120....
    3) Reply: If successful, then return "res=1&desc=ok", if fail, then return "res=0&desc=failure reasons".
      Example: http://api.iot.fm/upload.php?uid=10008&key=123&sensor_name=temperature&data=37&sensor_name=pluse&data=120
   After run the above Example, then return "res=1&desc=ok".

  * Using TCP protocol including the following steps
    1) Using Socket connection
    2)





