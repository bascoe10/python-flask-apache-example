# Python Flask Apache Example

## Apache Installation
[Apache](http://httpd.apache.org/docs/2.4/install.html)
- sudo yum install httpd
- sudo systemctl enable httpd
- sudo systemctl start httpd

### side note - setup public dir
- cd /var/www/
- mkdir public_html
- sudo chown -R $USER:$USER /var/www/public_html/ 

## Apache Config file
- sudo vim /etc/httpd/conf.d/public_html.conf
- - see _apache.conf_ for content
- sudo systemctl restart httpd

### side note - pip install
- curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
- python get-pip.py

## WSGI setup
- sudo yum install mod_wsgi
- sudo systemctl restart httpd

### side note - verify installation of wsgi
- sudo httpd -M | grep wsgi

## Flask Install
- pip install flask
- create flask application in a fashion similar to _myapplication_

## Final setup
- create a _wsgi_ file. 
- see _myapplication/myapplication.wsgi_
