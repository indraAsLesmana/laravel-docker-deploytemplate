|-app/
|--|projectfile
|-nginx/
|--|conf.d
|----|default.conf
|-php/
|--|Dockerfile
docker-compose.yml

1. clone project into folder *app* exp: ``composer create-project laravel/laravel app``
2. docker-compose build
3. docker-compose up -d

faq:
1. issue write access to *storage/logs* folder
fix permission on your host:
``sudo chown -R  www-data:www-data app/storage``
``sudo chmod -R 775 app/storage``

re-build and run
``docker-compose down``
``docker-compose up -d --build``

2. how to run php artisan
``docker-compose exec php bash``
``cd /var/www``
