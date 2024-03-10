![Static Badge](https://img.shields.io/badge/Python-blue)
![GitHub last commit](https://img.shields.io/github/last-commit/KirillZavadskiy/kittygram_final)
![GitHub repo size](https://img.shields.io/github/repo-size/KirillZavadskiy/kittygram_final)

# О проекте kittygram_final 
Проект **kittygram_final** - это сайт, на котором пользователь может зарегистрироватся и создать карточку своего котика. Главная страница, это лента с котиками и их именами. Перейдя в карточку котика, можно увидеть, кроме его имении, сколько ему полных лет и достижения, например, уронил елку или украл второй носок.

# Технологии. 
- djangorestframework 
- django 
- djoser
- gunicorn
- nginx

# Использование программы
1. Клонировать репозиторий 
```` 
git clone git@github.com:KirillZavadskiy/kittygram_final.git
```` 
2. Cоздать файл .env в корневой директории
```` 
POSTGRES_USER=
POSTGRES_PASSWORD=
POSTGRES_DB=
DB_HOST=db
DB_PORT=5432
SECRET_KEY=
DEBUG=False
ALLOWED_HOSTS=<'домен'>
```` 
3. Запустить файл docker-compose.production.yml
```` 
docker compose -f docker-compose.production.yml up --build
```` 
4. Выполнить миграции + статика
```` 
docker compose -f docker-compose.production.yml exec backend python manage.py migrate
docker compose -f docker-compose.production.yml exec backend python manage.py collectstatic
docker compose -f docker-compose.production.yml exec backend cp -r /app/collected_static/. /static/static/
```` 
# Автор
Кирилл Завадский
