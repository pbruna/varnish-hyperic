###Introduction
The Varnish plugin allows you to gather a series of metrics from one instance of Varnish HTTP accelerator, including availability, requests served, bytes served, cache hits a cache misses.

###Howto

##Instalation

1. Clone this repo
2. Install the Config::INI::Simple Perl Module on the agents
3. Stop the HQ Server and Agents
4. Copy the plugin to the respective plugin directory 

On HQ Server:
```bash
cp  varnish-plugin.xml <hq installation dir>/hq-plugins/
```

On HQ Agent:
```bash
cp  -a scripts/ varnish-plugin.xml <hq installation dir>/hq-plugins/
chmod +x /opt/hyperic/hq-plugins/scripts/varnishstat.pl
```

5. Give write permitions to the scripts directory to the user who runs the HQ Agent process
```bash
chmod o+w  /opt/hyperic/hq-plugins/scripts/
```

6. Restart the HQ Servers and Agents


