
# Checking Your Installation

## Check FreeTAKServer, FreeTAKServer-UI, and WebMap

Open a web browser to:

`http://[YOUR_IP_ADDRESS]:5000/`
default  <http://127.0.0.1:5000/>

- login with your credentials
  - by default is user: `admin`, password: `password`
  - you should promptly change the login credentials
    - [change profile password](../administration/Web_Admin.md) , or
    - [create a new user and delete `admin`](../administration/Web_Admin.md)
- check whether services are OK (blue)
![image](https://user-images.githubusercontent.com/60719165/148986287-0c83aa3f-e909-4b38-bc81-d66cddb08f89.png)
- connect a client to the server
- click on the WEBMAP button
- confirm the client is connected in the WEBMAP

## Check The Video Server

Open a web browser to:

`http://[YOUR_IP_ADDRESS]:9997/v1/config/get`
default  <http://127.0.0.1:9997/v1/config/get/>

Confirm the configuration (which is in `json` format):

```json
{
  "logLevel": "info",
  "logDestinations": [
    "stdout"
  ],
  "logFile": "mediamtx-server.log",
  "readTimeout": "10s",
  "writeTimeout": "10s",
  "readBufferCount": 512,
  "api": true,
  "apiAddress": "[YOUR_IP_ADDRESS]:9997",
  "metrics": false,
  "metricsAddress": "127.0.0.1:9998",
  "pprof": false,
  "pprofAddress": "127.0.0.1:9999",
  "runOnConnect": "",
  "runOnConnectRestart": false,
  "rtspDisable": false,
  "protocols": [
    "multicast",
    "tcp",
    "udp"
  ],
  "encryption": "no",
  "rtspAddress": ":8554",
  "rtspsAddress": ":8555",
  "rtpAddress": ":8000",
  "rtcpAddress": ":8001",
  "multicastIPRange": "224.1.0.0/16",
  "multicastRTPPort": 8002,
  "multicastRTCPPort": 8003,
  "serverKey": "server.key",
  "serverCert": "server.crt",
  "authMethods": [
    "basic",
    "digest"
  ],
  "readBufferSize": 2048,
  "rtmpDisable": false,
  "rtmpAddress": ":1935",
  "hlsDisable": false,
  "hlsAddress": ":8888",
  "hlsAlwaysRemux": false,
  "hlsSegmentCount": 3,
  "hlsSegmentDuration": "1s",
  "hlsAllowOrigin": "*",
  "paths": {
    "~^.*$": {
      "source": "publisher",
      "sourceProtocol": "automatic",
      "sourceAnyPortEnable": false,
      "sourceFingerprint": "",
      "sourceOnDemand": false,
      "sourceOnDemandStartTimeout": "10s",
      "sourceOnDemandCloseAfter": "10s",
      "sourceRedirect": "",
      "disablePublisherOverride": false,
      "fallback": "",
      "publishUser": "",
      "publishPass": "",
      "publishIPs": [],
      "readUser": "",
      "readPass": "",
      "readIPs": [],
      "runOnInit": "",
      "runOnInitRestart": false,
      "runOnDemand": "",
      "runOnDemandRestart": false,
      "runOnDemandStartTimeout": "10s",
      "runOnDemandCloseAfter": "10s",
      "runOnPublish": "",
      "runOnPublishRestart": false,
      "runOnRead": "",
      "runOnReadRestart": false
    }
  }
}
```

## Check the FreeTAKHub Server (or Node-RED Server)

Open a web browser to: 

`http://[YOUR_IP_ADDRESS]:1880/`
default  <http://127.0.0.1:1880/>

- login with your credentials
  - by default is user: `admin`, password: `password` (you should promptly change the default password) 
  - these are the same credentials used previously

see [NodeRed](../administration/brokered/Integration/NodeRedInstallation.md) for more information

## Check Voice server
connect a client to `[YOUR_IP_ADDRESS]:64738`
