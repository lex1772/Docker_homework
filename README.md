Домашняя работа 27.1 Основы Docker.
=====
### 1. Запуск контейнера с Python
Устанавливаем образ командой `docker pull python`

Запускаем контейнер командой `docker run --name django_project --it python`

Устанавливаем через консоль django

Запускаем приложение

Запускаем локальный сервер и убеждаемся, что все работает прекрасно


### 2. Запуск контейнера с PostgreSQL
Устанавливаем образ командой `docker pull postgres`

Запускаем контейнер и сохраняем данные локально командой `docker run -p 5432:5432 -e POSTGRES_PASSWORD=mysecretpassword -e POSTGRES_DB=public -e POSTGRES_HOST_AUTH_METHOD=md5 -v "Ваш путь":/var/lib/postgresql/data postgres`

В django settings.py добавляем базу данных

Запускаем, проверяем что сервер запустился

### 3. Запуск контейнера с Redis
Устанавливаем образ командой `docker pull redis`

Запускаем контейнер `docker run --name redis_django -d redis`

В django settings.py добавляем настройки для очередей celery

Домашняя работа 27.2 Docker Compose.
=====
Собираем образ с помощью команды `docker-compose build`

Запускаем контейнеры с помощью команды `docker-compose up`

Применяем миграции с помощью команды `docker-compose exec app python manage.py migrate`
