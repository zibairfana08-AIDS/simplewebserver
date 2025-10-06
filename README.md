# EX01 Developing a Simple Webserver
## Date:

## AIM:
To develop a simple webserver to serve html pages and display the Device Specifications of your Laptop.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
# EX01 Developing a Simple Webserver
## Date:17/9/2025

## AIM:
To develop a simple webserver to serve html pages and display the list of protocols in TCP/IP Protocol Suite.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
~~~
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>TCP/IP Protocol Suite Table</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f9f9f9;
      padding: 20px;
    }

    h1 {
      text-align: center;
      color: #333;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin-top: 20px;
      background-color: #fff;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }

    th, td {
      padding: 12px 15px;
      text-align: left;
      border-bottom: 1px solid #ddd;
    }

    th {
      background-color: #4CAF50;
      color: white;
    }

    tr:hover {
      background-color: #f1f1f1;
    }

    caption {
      caption-side: top;
      font-size: 1.2em;
      font-weight: bold;
      padding: 10px;
    }
  </style>
</head>
<body>

  <h1>TCP/IP Protocol Suite Table</h1>

  <table>
    <caption>Overview of TCP/IP Protocol Layers</caption>
    <thead>
      <tr>
        <th>TCP/IP Layer</th>
        <th>OSI Equivalent</th>
        <th>Common Protocols</th>
        <th>Functions</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Application Layer</td>
        <td>OSI Layers 5-7</td>
        <td>HTTP, HTTPS, FTP, SMTP, DNS, SSH, SNMP</td>
        <td>Provides services to user applications, including data formatting and encryption.</td>
      </tr>
      <tr>
        <td>Transport Layer</td>
        <td>OSI Layer 4</td>
        <td>TCP, UDP</td>
        <td>Reliable or fast delivery of data between devices; flow control, error checking.</td>
      </tr>
      <tr>
        <td>Internet Layer</td>
        <td>OSI Layer 3</td>
        <td>IP (IPv4/IPv6), ICMP, ARP</td>
        <td>Routing of packets across networks; addressing and fragmentation.</td>
      </tr>
      <tr>
        <td>Network Access Layer</td>
        <td>OSI Layers 1-2</td>
        <td>Ethernet, Wi-Fi, MAC, PPP</td>
        <td>Physical transmission of data; hardware addressing; error detection.</td>
      </tr>
    </tbody>
  </table>

</body>
</html>

"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
~~~

## OUTPUT:
<img width="1920" height="1080" alt="Screenshot (5)" src="https://github.com/user-attachments/assets/6cda008c-de43-4a85-b80b-74c95402fd0a" />

<img width="1920" height="1080" alt="Screenshot (6)" src="https://github.com/user-attachments/assets/af9770d4-f4ce-48a4-9c14-a0aa3d53b0b1" />

## RESULT:
The program for implementing simple webserver is executed successfully.

## OUTPUT:


## RESULT:
The program for implementing simple webserver is executed successfully.
