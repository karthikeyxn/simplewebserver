Skip to content
Navigation Menu
hariharana59
simplewebserver

Type / to search
Code
Pull requests
Actions
Projects
Security
Insights
Owner avatar
simplewebserver
Public
forked from selvasachein/simplewebserver
hariharana59/simplewebserver
Go to file
t
This branch is 6 commits ahead of, 2 commits behind selvasachein/simplewebserver:main.
Name		
hariharana59
hariharana59
Update README.md
8c82b00
 · 
last year
snmp
sucess
last year
README.md
Update README.md
last year
jerry.py
sucess
last year
Repository files navigation
README
EX01 Developing a Simple Webserver
Date:14.02.2024
AIM:
To develop a simple webserver to serve html pages.

DESIGN STEPS:
Step 1:
HTML content creation.

Step 2:
Design of webserver workflow.

Step 3:
Implementation using Python code.

Step 4:
Serving the HTML pages.

Step 5:
Testing the webserver.

PROGRAM:
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>Software Companies</title>
</head>
<body bgcolor="cyan">
<table border="4" cellspacing="1" cellpadling="1" height="300" width="700" bgcolor="white">
<caption>TOP SOFTWARE COMPANIES WITH REVENUE</caption>
		<tr>
			<th>COMPANY</th>
			<th>REVENUE</th>
			<th>PERCENTAGE</th>
		</tr>
		<tr>
			<td>Google</td>
			<td>4541397</td>
			<td>1</td>
		</tr>

		<tr>
			<td>Meta</td>
			<td>3216464</td>
			<td>2</td>
		</tr>

		<tr>
			<td>SAMSUNG</td>
			<td>1649465</td>
			<td>3</td>
		</tr>
                 <tr>
			<td>TCS</td>
			<td>51918518</td>
			<td>4</td>
		</tr>

                 <tr>
			<td>Infosys</td>
			<td>5191587</td>
			<td>5</td>
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
Screenshot 2024-03-12 113439

Screenshot 2024-03-12 113654

RESULT:
The program for implementing simple webserver is executed successfully.

About
No description, website, or topics provided.
Resources
 Readme
 Activity
Stars
 1 star
Watchers
 0 watching
Forks
 1 fork
Report repository
Releases
No releases published
Packages
No packages published
Languages
Python
99.1%
 
HTML
0.9%
Footer
© 2025 GitHub, Inc.
Footer navigation
Terms
Privacy
Security
Status
Docs
Contact
Manage cookies
Do not share my personal information
Editing simplewebserver/README.md at main · hariharana59/simplewebserver
