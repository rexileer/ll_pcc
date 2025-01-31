# Django Learning Log

Этот проект представляет собой веб-приложение для ведения записей о процессе обучения. Он построен на Django 4.1.1 и использует Bootstrap, SQLite (по умолчанию) и Heroku для деплоя.

## Установка и запуск

### 1. Клонирование репозитория
```sh
git clone <репозиторий>
cd learning_log
```

### 2. Создание и активация виртуального окружения
```sh
python -m venv venv
source venv/bin/activate  # (Windows: venv\Scripts\activate)
```

### 3. Установка зависимостей
```sh
pip install -r requirements.txt
```

### 4. Настройка базы данных
По умолчанию используется SQLite. Для её инициализации выполните:
```sh
python manage.py migrate
```
Если требуется использовать PostgreSQL, настройте переменные окружения:
```sh
export DATABASE_URL='postgres://user:password@localhost:5432/dbname'
```
Или укажите в `.env` файле.

### 5. Запуск сервера разработки
```sh
python manage.py runserver
```

## Деплой на Heroku
### 1. Установка Heroku CLI и вход в аккаунт
```sh
heroku login
```
### 2. Создание Heroku-приложения
```sh
heroku create <app-name>
```
### 3. Настройка и деплой
```sh
git push heroku main
heroku run python manage.py migrate
heroku open
```

## Используемые технологии
- Django 4.1.1
- SQLite (по умолчанию) / PostgreSQL (при деплое на Heroku)
- Bootstrap 4
- Heroku
- Gunicorn
- Whitenoise (для статических файлов)

## Лицензия
Этот проект распространяется под лицензией MIT.

