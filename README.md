# AnaviInfraredPhat

## AnaviInfraredPhat as an application

Publishes temperature, pressure, humidity, luminosity and heat index from your Pi over 0MQ.

```
python3 -m AnaviInfraredPhat --verbose
2019-05-12 10:40:19.192 JST [   DEBUG] __init__ : Logging with global level DEBUG
2019-05-12 10:40:19.196 JST [   DEBUG] __init__ : Sysout logging with level DEBUG
2019-05-12 10:40:19.199 JST [   DEBUG] __init__ : Changing sysout format to logfile
2019-05-12 10:40:19.217 JST [   DEBUG] __init__ : Added TimedRotatingFileHandler to /var/logAnaviInfraredPhat.log with level DEBUG.
2019-05-12 10:40:19.228 JST [   DEBUG] __init__ : Log rotates every D and keeps 15 logs.
2019-05-12 10:40:19.233 JST [    INFO] __main__ : Starting
2019-05-12 10:40:20.093 JST [   DEBUG] __main__ : {"hi": null, "l": 63, "hi_cmt": "No concerns", "h": 42, "p": 1015, "t": 25.8}
```

## AnaviInfraredPhat as a module

The module can be used from a different machine than the Raspberry Pi hosting the Anavi Infrared Phat.

It has a class for each sensor provided with the original Anavi Infrared Phat Kit.

* BH1750
* HTU21D
* BMP180

As well as a class to emit IR codes.

* IRSEND (adapted from Joan's script @ http://abyz.co.uk/rpi/pigpio/code/irrp_py.zip. It uses records files which are to be created with irrp.py)

Some more functions are available as example or boilerplate code:

* report_tphl
* report_tphl_average
* report_tphl_as_text

Please refer to the code.