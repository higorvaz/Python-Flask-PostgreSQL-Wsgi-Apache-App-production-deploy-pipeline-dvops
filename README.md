## Make a development Python VENV to Production

### Python App production deploy test on Linux Debian cloud

First stop Apache, if installed.

#### Files structure

![](https://user-images.githubusercontent.com/9384127/230894921-8a13d915-022e-4343-afbe-01009548ff83.png)

*   nano -lASimYpython app.py

![](https://user-images.githubusercontent.com/9384127/230911418-56db5b90-643b-4b4a-8b86-29c723b303e7.png)

*   nano -lASimYpython wsgi.py

![](https://user-images.githubusercontent.com/9384127/230911909-78a90717-b9ec-43e3-9e70-78244d76bb3c.png)

#### Create and activate the venv source

*   virtualenv env
*   source env/bin/activate

(env) root@localhost:/home/python-flask-production-app#

#### Requirements

*   pip install Flask
*   pip install mod-wsgi-httpd
*   pip install mod-wsgi

#### Configure

*   (env) root@localhost:/home/python-flask-production-app# mod\_wsgi-express setup-server wsgi.py --port=80 --user www-data --group www-data --server-root=/etc/mod\_wsgi-express-80

![](https://user-images.githubusercontent.com/9384127/230905418-11e82dbf-be28-4de3-8748-d8857eee2155.png)

#### Run

*   /etc/mod\_wsgi-express-80/apachectl start

![](https://user-images.githubusercontent.com/9384127/230910229-3a0ac85c-a045-4e9b-b06d-1f45de156fba.png)
