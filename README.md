# Developing a Simple Webserver

# AIM:
NAME:Aldrin Lijo REFno:22008844

Develop a webserver to display about top five web application development frameworks.

# DESIGN STEPS:

## Step 1:

HTML content creation is done

## Step 2:

Design of webserver workflow

## Step 3:

Implementation using Python code

## Step 4:

Serving the HTML pages.

## Step 5:

Testing the webserver

# PROGRAM:
```py
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
</head>
<body>
<h1>SIMPLE WEBSERVER</h1>
</body>
</html>
"""

class Hellohandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('content type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

server_address = ('',80)
httpd = HTTPServer(server_address, Hellohandler)
print("server is running")
httpd.serve_forever()
```

# OUTPUT:
SERVER SIDE OUTPUT:
![output](/Screenshot%20from%202023-01-06%2013-37-34.png)
CLIENT SIDE OUTPUT:
![output](/Screenshot%20from%202023-01-06%2013-22-03.png)
# RESULT:

The program is executed succesfully
