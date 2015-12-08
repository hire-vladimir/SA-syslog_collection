# Getting Started
You are in the right place if your looking to configure *rsyslog* for remote collection.

## Pre-requisites
* **root** or **sudo** access to instance
* rsyslog version 5.0 or higher
* `/etc/rsyslog.conf` file containing following line `$IncludeConfig /etc/rsyslog.d/*.conf`

## Enabling remote syslog collection
1. Ensure pre-requisites are met
2. Place included `appserver/config/splunk.rsyslog.conf` in `/etc/rsyslog.d/`, modifying as needed
3. Restart syslog daemon, follow *Applying changes* section for how-to

## Applying changes
To apply configuration changes, the syslog daemon needs to be restarted by running `service rsyslog restart`

# Troubleshooting
See README.md

### Checking version
```
root@x /v/log# which rsyslogd
/usr/sbin/rsyslogd
root@x /v/log#
root@x /v/log# rsyslogd -version
rsyslogd 7.4.7, compiled with:
        FEATURE_REGEXP:                         Yes
        FEATURE_LARGEFILE:                      No
        GSSAPI Kerberos 5 support:              Yes
        FEATURE_DEBUG (debug build, slow code): No
        32bit Atomic operations supported:      Yes
        64bit Atomic operations supported:      Yes
        Runtime Instrumentation (slow code):    No
        uuid support:                           Yes

See http://www.rsyslog.com for more information.
root@x /v/log#
```

# Additional reference
Following documentation are great reference material:
* rsyslog properties - http://www.rsyslog.com/doc/master/configuration/properties.html
* rsyslog filters - http://www.rsyslog.com/doc/v8-stable/configuration/filters.html
