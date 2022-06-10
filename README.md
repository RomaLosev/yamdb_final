![example workflow](https://github.com/huli-net/yamdb_final/actions/workflows/yamdb_workflow.yaml/badge.svg)

API_YAMDB

API_YAMDB - проект учебного API для сервиса отзывов к произведениям

АВТОРЫ:

Роман Лосев - https://github.com/huli-net

ЗАПУСК ПРОЕКТА


### Клонировать репозиторий 

### Заполнить файл .env

DB_ENGINE= <База данных с которой будем работать>
DB_NAME= <Имя базы данных>
POSTGRES_USER= <Логин для подключения к базе данных>
POSTGRES_PASSWORD= <Пароль для подключения к БД>
DB_HOST= <Название сервиса>
DB_PORT= <Порт для подключения к БД>

### Запустить проект

1. docker-compose up -d --build #Создание контейнера
2. docker-compose exec web python manage.py migrate #Миграции
3. docker-compose exec web python manage.py createsuperuse r  #Создание пользователя с правами суперюзера
4. docker-compose exec web python manage.py collectstatic --no-input #Загрузка статики