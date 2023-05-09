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

from http.server import HTTPServer, BaseHTTPRequestHandler

content = """

<!DOCTYPE html>

<html>

    <head>

        <title>My webserver</title>

    </head>

    <body>

        <h1><u>Languages used iun Web Development</u><h1>

            <ul>

                <li>HTML</li>

                <li>CSS</li>

                <li>JavaScript</li>

                <li>Bootstrap</li>

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

            server_address = ('',80)

            httpd = HTTPServer(server_address,myhandler)

            print("my webserver is running...")

            httpd.serve_forever()


## OUTPUT:
![229406761-572c496d-940d-495c-8831-c68e5f5d0b4a](https://github.com/vijayarajv1704/webserver/assets/121303741/7f529cee-c595-42ad-85ce-d5b82836061f)

![Screenshot 2023-05-09 190738](https://github.com/vijayarajv1704/webserver/assets/121303741/156dc328-4dbf-44b8-b84a-9eeb3623f570)

## RESULT:
The program is executed succesfully
