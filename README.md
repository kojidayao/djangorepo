# api
- Run cli using linux environment. For windows use **Git Bash**
- Install **virtualenv** package `pip install virtualenv` If ubuntu `sudo apt install python3-venv`.
- Run `virtualenv env`. Please make sure outside root directory project. If ubuntu `python3 -m venv env`.
- Copy/Paste *requirements.txt* and *secrets.sh* outside root directory project
- Run `source env/Scripts/activate`. If ubuntu `source env/bin/activate`.
- Run `pip install -r requirements.txt`. If ubuntu `pip install -r requirements_ubuntu.txt`.
- Run `touch secrets.sh`
- Exit from virtualenv by typing `deactivate`
- Go to root directory project `cd core-api`
- Create `yakaph.config` file
- Inside the file, paste the following and enter your postgres password
```
[database-config]
name=yakaph_dev
user=postgres
password=YOUR_PASSWORD
host=127.0.0.1
```
- Run `python manage.py makemigrations`
- Run `python manage.py migrate`
- Run `python manage.py runserver`

**OPTIONAL**
- Create super user run `python manage.py createsuperuser` to login admin site
- Updating *requirements.txt* run `pip freeze > requirements.txt`

