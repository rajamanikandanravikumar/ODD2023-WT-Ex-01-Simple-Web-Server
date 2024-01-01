# Ex-01-Simple-Web-Server
## Date:

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:
`````
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
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())


server_address = ('', 80)
httpd = HTTPServer(server_address, HelloHandler)
httpd.serve_forever()
''''''


## OUTPUT:
![Screenshot 2024-01-01 214350](https://github.com/rajamanikandanravikumar/ODD2023-WT-Ex-01-Simple-Web-Server/assets/145742839/8ee71cd6-d689-43d2-b2ce-56a9b70682e3)





## RESULT:
The program for implementing simple webserver is executed successfully.
