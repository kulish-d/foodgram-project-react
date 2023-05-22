# Продуктовый помощник - Foodgram

### http://158.160.8.172/

Доступ к админке:
yandex@shmail.com
yandex


### To deploy this project need the next actions:
- Скачиваем проект
```
git clone https://github.com/kulish-d/foodgram-project-react.git
```
- Подключаемся к серверу
```
ssh <server user>@<public server IP>
```
- Устанавливаем докер
```
sudo apt install docker.io
```
- Устанавливаем Docker-Compose (для Linux)
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
- Получаем права для docker-compose
```
sudo chmod +x /usr/local/bin/docker-compose
```
- Скидываем файлы docker-compose.yaml и nginx.conf на сервер, сделать это можно командой (в случае удаленного запуска)
```
scp docker-compose.yaml <username>@<public ip adress>:/home/<username>/docker-compose.yaml
```
- Создать env:
```
touch .env
```
- Заполнить env/github secrets:
```
DOCKER_USERNAME - имя пользователя в DockerHub
DOCKER_PASSWORD - пароль пользователя в DockerHub
HOST - ip-адрес сервера
USER - пользователь
SSH_KEY - приватный ssh-ключ (публичный должен быть на сервере)
PASSPHRASE - кодовая фраза для ssh-ключа
DB_ENGINE - django.db.backends.postgresql
DB_HOST - db
DB_PORT - 5432
SECRET_KEY - секретный ключ приложения django (необходимо чтобы были экранированы или отсутствовали скобки)
ALLOWED_HOSTS - список разрешённых адресов
TELEGRAM_TO - id своего телеграм-аккаунта (можно узнать у @userinfobot, команда /start)
TELEGRAM_TOKEN - токен бота (получить токен можно у @BotFather, /token, имя бота)
DB_NAME - postgres (по умолчанию)
POSTGRES_USER - postgres (по умолчанию)
POSTGRES_PASSWORD - postgres (по умолчанию)
```