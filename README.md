# Service_app
Учебный проект по оптимизации Django

### Установка и запуск с помощью Docker-compose:
Клонируйте репозиторий:
```shell
git clone https://github.com/evgen4ikrus/service_app.git
```

Скачайте и соберите докер-образы с помощью Docker-Сompose:
```shell
docker-compose build
```

Запустите докер-контейнеры:
```shell
docker compose up
```

В новом терминале накатите свежие миграции БД:
```shell
docker-compose run --rm web-app sh -c "python manage.py migrate"
```
Если всё сделано правильно, то вход в админку будет доступен по адресу http://127.0.0.1:8000/admin/

Для создания суперпользователя воспользуйтесь командой:
```shell
docker-compose run --rm web-app sh -c "python manage.py createsuperuser"
```

### Полезные ссылки:
[Админка](http://127.0.0.1:8000/admin/), [API](http://127.0.0.1:8000/api/subscriptions/?format=json), [Flower](http://127.0.0.1:5555/).