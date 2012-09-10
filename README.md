# check_statsd.py

#### Requirements
* pynagios==0.1.1

#### Installation
1. Install pynagios
```
    pip install pynagios
```

2. Clone statsd-nagios-plugin
```
    git clone git://github.com/saz/statsd-nagios-plugin.git
```

#### Usage

**Check if uptime is higher than 60 seconds (critical) and 300 seconds (warning)**

    python check_statsd.py -H <hostname> -p <port> -w '300:~' -c '60:~'

**Check if uptime is lower than 1600000 seconds (critical) and 1300000 seconds (warning)**

    python check_statsd.py -H <hostname> -p <port> -w '~:1300000' -c '~:1600000'
