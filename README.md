# szrt
Simple Zabbix Remediation Tool

## Sumary
The ideia behind this is provide a set of tools that brings scalabilitie
for dealing with remediation issues in zabbix.

## Components
* Standalone request script ( The Bridge )
* Remediation Router (Webservice)
* Remediation Dispatcher (Jobs dispatcher)
* Remediation Library ( Remediation Catalog)
* Remediation Patch (standalone runner)
 
### Standalone request script
This tool is responsible to build the bridge between zabbix and the webservice
that will route the event (triggers) for our remediation router.

### Remediation Router
Will validate if the trigger matches our catalog and place a job for it

### Remediation Dispatcher
Consume a queue that will apply our remediation

### Remediation Library
Catalog that matches the trigger with its remediation rule

### Remediation Runner
Standalone service that matches the trigger with its remediation and
play the action to fix the issue
