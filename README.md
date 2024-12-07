# EX01 Developing a Simple Webserver

# Date:
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<html>
<head>
<title>Top 5 Software companines in revenue</title>
<head>
<body>
<h1 align="center">Top Software Companies<h1>
<table border="2" cellspacing="4" cellpadding="6">
<tr>
<th>S.no</th>
<th>Comany</th>
<th>Revenue</th>
<tr>
<tr>
<td>1</td>
<td>Apple</td>
<td>$385.70 B </td>
</tr>
<td>2</td>
<td>Google</td>
<td>$307.39 B</td>
</tr>
<td>3</td>
<td>Microsoft</td>
<td>$227.58 B</td>
</tr>
<td>4</td>
<td>IBM</td>
<td>$61.85 B</td>
</tr>
<td>5</td>
<td>Oracle</td>
<td>$51.62 B</td>
</tr>
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

OUTPUT:
alt text
```

alt text
# OUTPUT:


![Screenshot 2024-12-05 083003](https://github.com/user-attachments/assets/aef85e0c-b9c7-4148-b208-f9600453e760)
![Screenshot 2024-12-07 161350](https://github.com/user-attachments/assets/aa41bdc0-8473-4c43-9fb8-562d249e34a0)





# RESULT:
The program for implementing simple webserver is executed successfully.
