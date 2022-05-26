# Django database settings


- [PostgreSQL](#postgresql)

- [MySQL](#mysql)

- [Oracle](#oracle)

- [MongoDB (Djongo)](#mongodb-djongo)

- [SQLite](#sqlite)

---
## PostgreSQL
<img src="https://upload.wikimedia.org/wikipedia/commons/2/29/Postgresql_elephant.svg" width="250" alt="PostgreSQL_img">

### Install

```
pip install psycopg2
```

### Use

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',

        'NAME': '<db_name>',

        'USER': '<db_username>',

        'PASSWORD': '<password>',

        'HOST': 'localhost',

        'PORT': '5432',
    }
}
```

---
## MySQL
<img src="https://www.vectorlogo.zone/logos/mysql/mysql-official.svg" width="250" alt="MySQL_img">

### Install

```
pip install mysqlclient
```

### Use

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',

        'NAME': '<db_name>',

        'USER': '<db_username>',

        'PASSWORD': '<password>',

        'HOST': 'localhost',
        
        'PORT': '3306',
    }
}
```

---
## Oracle
<img src="https://upload.wikimedia.org/wikipedia/commons/2/29/Oracle_wordmark.svg" width="250"  alt="Oracle_img">

### Install

```
pip install cx_Oracle
```

### Use

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.oracle',

        'NAME': '<db_name>',

        'USER': '<db_username>',

        'PASSWORD': '<password>',

        'HOST': 'localhost',

        'PORT': '1540',
    }
}
```
---

## MongoDB (Djongo)
<img src="https://upload.wikimedia.org/wikipedia/commons/9/93/MongoDB_Logo.svg" width="250"  alt="MongoDB_img">

### Install

```
pip install djongo
```

### Use
```python
DATABASES = {
    'default': {
        'ENGINE': 'djongo',
        
        'NAME': '<db_name>',
    }
}
```

OR

```python
DATABASES = {
    'default': {
        'ENGINE': 'djongo',
        
        'NAME': '<db_name>',
        
        'ENFORCE_SCHEMA': False,
        
        'CLIENT': {
            'host': 'mongodb+srv://<db_username>:<password>@<atlas cluster>/<myFirstDatabase>?retryWrites=true&w=majority'
        }
    }
}
```

---
## SQLite
<img src="https://upload.wikimedia.org/wikipedia/commons/3/38/SQLite370.svg" width="250"  alt="SQLite_img">

### Use

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}
```
