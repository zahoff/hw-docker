Решение домашнего задания к лекции Docker

Задача 1 / task1
Приложены файлы Dockerfile и index.html
Для сборки образа:
запустить терминал в папке со скачанными файлами
выполнить команду docker build -t new_nginx .
Запустить контейнер командой docker run  -d name=my_nginx new_nginx
Также образ был загружен на dockerhub. 
Скачать и запустить можно выполнив команды:
docker pull headsoft/netology_homework:new_nginx_latest
docker run -d name=my_nginx headsoft/netology_homework
По адресу http://localhost:80 открывается страница "nginx docker test" с надписью Hello World!

Задача 2 / task2
В settings.py в ALLOWED_HOSTS записаны "localhost", "127.0.0.1", а также внесены изменения в DATABASES для работы с sqlite3
Обновлен файл requirements.txt: pip freeze>requirements.txt
Создан файл Dockerfile
Создан файл .dockerignore, в котором указаны файлы, которые не нужно копировать в образ
Для того чтобы создать контейнер для REST API сервера нужно выполнить команду (из директории проекта): docker build -t django_project .
Для запуска контейнера нужно выполнить команду:
run --name=django_test -d -p 8000:8000 django_project
Для проверки работоспособности можно получить список продуктов (GET-запрос) здесь: http://localhost:8000/api/v1/products/, 
Или отправить запрос из файла requests-examples.http.
