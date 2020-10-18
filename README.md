# Flask init template
---------------------
This is a simple init template base to start building services with Python Flask.

---

### Run the API
---------------
Start both the services (DB & API) with Docker
```bash
docker-compose up -d
```
and API will be available at ```localhost:8080```

To run the API locally
```
virtualenv -p python3 venv && . venv/bin/activate
pip3 install -r requirements/dev.txt
flask run -p 8080
```
then the API will be available at ```localhost:5000```

---

### Env variables
--------------------
```bash
export FLASK_APP=api
export FLASK_DEBUG=1
export APP_SETTINGS=Development
export FLASK_ENV=development
export SECRET_KEY=this-really-needs-to-be-changed
export DATABASE_URL=postgresql+psycopg2://hades:d0nt4get@postgres:5432/hades
```
if the API is started with ```flask run``` then
```bash
export DATABASE_URL=postgresql+psycopg2://hades:d0nt4get@localhost:5432/hades
```

---

### Documentation
-----------------
The Swagger documentation is available @[flask-init-template.herokuapp.com](https://flask-init-template.herokuapp.com/swagger)
or alternatively, at the development stage, @```localhost:<port>/swagger```

---

### Optimizations
-----------------
A more optimized setup with [uWSGI-NGINX](https://flask.palletsprojects.com/en/1.1.x/deploying/uwsgi/).

Standalone [WSGI Containers](https://flask.palletsprojects.com/en/1.1.x/deploying/wsgi-standalone/).