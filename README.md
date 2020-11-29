# API REST con Django-Rest-Framework para fruver


#### Crear proyecto

```sh
$ mkdir fruver_svc
$ cd fruver_svc
$ virtualenv . -p python3
$ mkdir src
$ cd src
```

#### Aplicar requerimientos
```sh
$ source ../bin/activate
$ (fruver_svc) pip install -r requirements.txt
```

#### Configurar base de datos
```sh
DATABASES = {
    'default': {
            'ENGINE': 'django.db.backends.postgresql_psycopg',
            'NAME': 'fruver_db',
            'USER': 'admin',
            'PASSWORD': 'secret',
            'HOST': '0.0.0.0',
            'PORT': '5432',
        }
}
```
 
### Crear proyecto y apps
En cada carpeta nueva que se crea en el project no olvidar el archivo __init__.py si no se crea
automaticamente, para que Django reconozca el directorio como parte del proyecto
```sh
$ (fruver_svc) cd src/
$ (fruver_svc) django-admin startproject fruver
$ (fruver_svc) cd fruver/
$ (fruver_svc) mkdir apps/
$ (fruver_svc) cd apps/
$ (fruver_svc) django-admin startapp products_providers

```

#### Aplicar migraciones

```sh
$ (fruver_svc) cd src/
$ (fruver_svc) python manage.py makemigrations
$ (fruver_svc) python manage.py migrate
```

#### Iniciar
```sh
$ (fruver_svc) python manage.py runserver
```