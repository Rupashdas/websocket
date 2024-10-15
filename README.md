
# WebSocket SSL (WSS) Setup Issue on Apache

## Overview

We have set up a WebSocket server using PHP and the Ratchet library. The server works fine on `localhost` using a non-SSL connection (`ws://`). However, we're encountering issues when trying to run the WebSocket server with SSL (`wss://`) on our live server.

### Current Problem

The WebSocket server is running successfully, but the browser console shows the following error when trying to establish a connection over SSL (`wss://`):


### Screenshots

1. **WebSocket Server Running (SSH Terminal)**:  
   ![WebSocket Server Running](https://github.com/user-attachments/assets/1b8b021c-d983-4a91-9134-aeed5aee837d)

2. **Browser Console Error**:  
   ![Browser Console Error](https://github.com/user-attachments/assets/d1069cc1-b231-4840-95a7-16ee5815e0d4)


### Code to Test WebSocket Connection

You can use the following code in your browser console to test the WebSocket connection:

```javascript
var conn = new WebSocket('wss://peakacademiccoaching.com:8080');
conn.onopen = function(e) {
    console.log("Connection established!");
};

conn.onmessage = function(e) {
    console.log(e.data);
};
```
### What We Need

We believe there might be an issue with the Apache server configuration related to handling SSL connections for WebSockets. We are looking for someone with experience in this area who can:

- Review the existing setup
- Diagnose the issue causing the SSL WebSocket connection to fail
- Fix the Apache configuration or identify any other issues preventing the WebSocket SSL connection from working

If you have experience with configuring SSL for WebSockets on Apache and can help resolve this issue, please reach out.

