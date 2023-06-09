<div align="center">
<img src="static/img/logo.png">
<h1>Indestructables</h1>
An open source alternative front-end to Instructables

<a href="https://indestructables.codeberg.page/">Website</a>
&nbsp;•&nbsp;
<a href="https://matrix.to/#/#indestructables-general:fedora.im">Matrix</a>
</div>

# Instances
See [here](https://indestructables.codeberg.page/#instances)

# Run your own instance

## Step by step installation

### Dependencies
`pip3 install -r requirements.txt`.

For the production environment, you also need the uWSGI Python3 plugin. On Debian, it can be installed via `apt install uwsgi-plugin-python3`
### Production
1. Clone the repository
2. Run `uwsgi --plugin python3 --http-socket 0.0.0.0:8002 --wsgi-file main.py --callable app --processes 4 --threads 2`
3. Point your reverse proxy to http://localhost:8002
### Development
1. Clone the repository
2. Run `python3 main.py`
3. Connect to http://localhost:8002

## Docker installation

`docker build --tag indestructables .`

`docker run -d -p 5000:5000 indestructables`