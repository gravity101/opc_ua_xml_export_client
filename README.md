OPC UA XML Export client
=========================

This client exports all nodes from a running OPC UA server into a node XML file

Dependencies
------------
* Python3
* opcua-asyncio v0.9.98 (https://github.com/FreeOpcUa/opcua-asyncio)
* progressbar2 (https://pypi.org/project/progressbar2/)

Install
-------
```bash
pip install asyncua
pip install progressbar2
```


Run
---
Export nodes from server `opc.tcp://localhost:16664` into XML file `export.xml`
```
python3 NodeXmlExporter.py opc.tcp://localhost:16664 export.xml

# Export only namespace 2
python3 NodeXmlExporter.py opc.tcp://localhost:16664 --namespace 2 export-ns2.xml

# Export with username/password
python NodeXmlExporter.py opc.tcp://localhost:16664 --namespace 2 -u myusername -p somestrongpassword export-ns2.xml
```
hey henrik
