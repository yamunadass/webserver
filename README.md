# Developing a Simple Webserver

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
</head>
<body>
<h1>Welcome</h1>
</body>
</html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(contet.encode())

server_addrress = ('',80)
httpd = HTTPServer(server_address,HelloHandler)
httpd.serve_forever()
```

## OUTPUT:
![image](https://github.com/yamunadass/webserver/assets/138971172/9a4dfde8-e6e0-41a7-b073-10a92763ccc4)

## RESULT:
The program is executed succesfully
