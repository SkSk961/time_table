# Ex03 Time Table
# Date:12/10/2024
# AIM
To write a html webpage page to display your slot timetable.

# ALGORITHM
## STEP 1
Create a Django-admin Interface.

## STEP 2
Create a static folder and inert HTML code.

## STEP 3
Create a simple table using <table> tag in html.

## STEP 4
Add header row using `<th>` tag.

## STEP 5
Add your timetable using `<td>` tag.

## STEP 6
Execute the program using runserver command.

# PROGRAM
~~~
from django.shortcuts import render
from http.server import BaseHTTPRequestHandler, HTTPServer
from importlib.resources import contents
from django.http import HttpResponse

content='''
<html>
<head>
    <title>slot timetable</title>
</head>
<body>
    <center> 
        <img src="Screenshot 2024-12-02 142946.png" height="100" width="500">
        <br>
        <table align="center" width="500" cellsapacing="2" cellpadding="5" border="5">
            <caption><b>SLOT TIME TABLE - SHARAN KUMAR G (24001249)</b></caption>
            <tr align="center">
                <th bgcolor="green">DAY/TIME</th>
                <th bgcolor="green">MONDAY</th>
                <th bgcolor="green">TUESDAY</th>
                <th bgcolor="green">WEDNESDAY</th>
                <th bgcolor="green">THURSDAY</th>
                <th bgcolor="green">FRIDAY</th>
                <th bgcolor="green">SATURDAY</th>
            </tr>
            <tr align="center">
                <th bgcolor="Red">8-10</th>
                <td bgcolor="blue">free slot</td>
                <td bgcolor="blue">free slot</td>
                <td bgcolor="blue">free slot</td>
                <td bgcolor="blue">physics</td>
                <td bgcolor="yellow">engineering mechanics and product develoment</td>
                <td bgcolor="blue">free slot</td>
            </tr>
            <tr align="center">
                <th bgcolor="Red">10-12</th>
                <td bgcolor="blue">basic electrical electronics and measurement engineering</td>
                <td bgcolor="blue">basic electrical electronics and measurement engineering</td>
                <td bgcolor="blue">career development</td>
                <td bgcolor="blue">c program</td>
                <td bgcolor="blue">fundamentals of web application</td>   
                <td bgcolor="blue"></td>/td>fundamentals of web application</td> 
            </tr>
            <tr align="center">
                <th bgcolor="Red">1-3</th>
                <td bgcolor="blue">fundamentals of web application</td>
                <td bgcolor="blue">c program</td>
                <td bgcolor="blue">mentor meeting</td>
                <td bgcolor="blue">free slot</td>
                <td bgcolor="blue">physics</td>   
                <td bgcolor="blue">engineering mechanics and product develoment</td> 
            </tr>
            <tr align="center">
                <th bgcolor="Red">3-5</th>
                <td bgcolor="yellow">Free slot</td>
                <td bgcolor="yellow">Free slot</td>
                <td bgcolor="yellow">Free slot</td>
                <td bgcolor="blue">c Programming</td>
                <td bgcolor="yellow">Free slot</td>   
                <td bgcolor="yellow">Free slot</td> 
            </tr>
        </table>
        <br>
        <table align="center" cellspacing="2" cellpadding="5" border="5">
            <tr align="center">
                <th>s. No.</th>
                <th>Subject Code</th>
                <th>Subject Name</th>
            </tr>
            <tr>
                <td align="center">1.</td>
                <td align="center">19AI414</td>
                <td>Fundamental of Web Application Development</td>
            </tr>
            <tr>
                <td align="center">2.</td>
                <td align="center">19AI301</td>
                <td>c Programming</td>
            </tr>
            <tr>
                <td align="center">3.</td>
                <td align="center">19CS405</td>
                <td>engineering mechanics and product develoment</td>
            </tr>
            <tr>
                <td align="center">4.</td>
                <td align="center">19CS406</td>
                <td>basic electrical electronics and measurement engineerin</td>
            </tr>
            <tr>
                <td align="center">5.</td>
                <td align="center">19CY205</td>
                <td>physics</td>
            </tr>
            <tr>
                <td align="center">6.</td>
                <td align="center">19EE404</td>
                <td>career development</td>
            </tr>
            <tr>
                <td align="center">7.</td>
                <td align="center">19EY702</td>
                <td>mentor meeting</td>
            </tr>
        </table>
    </center>
</body>
</html>

'''
from http.server import HTTPServer,BaseHTTPRequestHandler
class Myserver(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200)
        self.send_header("content-type","text/html")
        self.end_headers()
        self.wfile.write(content.encode())
print("This is my webserver")
server_address = ('',8000)
httpd = HTTPServer(server_address,Myserver)
httpd.serve_forever()
~~~
# OUTPUT
![Screenshot 2024-12-07 104306](https://github.com/user-attachments/assets/1c0cef39-d2ef-460e-a737-00c95f0b0fa9)
![get](https://github.com/user-attachments/assets/19f8c662-5963-46de-b427-59593095afbb)

# RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.
