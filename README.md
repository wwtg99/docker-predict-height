# docker-image-filter

## Description
Docker image for [height_predictor server](https://github.com/wwtg99/height_predictor) and [predict_height tool](https://github.com/wwtg99/predict_height). It is quickly to build a predict height demo service.

## Usage
Run image

```
docker run -d --name predict-height -p 8080:80  wwtg99/docker-predict-height:latest
```

Other usages refers to base image [docker-nginx-php](https://hub.docker.com/r/wwtg99/docker-nginx-php7).

## Environment
Config service for height_predictor server (see [Laravel](https://laravel.com/docs/5.6/configuration)). No need to change for most case.

- CACHE_DRIVER
- SESSION_DRIVER
- REDIS_HOST
- REDIS_PWD
- REDIS_PORT

Set timezone: TZ

```
docker run -d --name predict-height -p 8080:80 -e "TZ=Asia/Shanghai"  wwtg99/docker-predict-height:latest
```

Set server domain for default config: DOMAIN

```
docker run -d --name predict-height -p 8080:80 -e "DOMAIN=test.com"  wwtg99/docker-predict-height:latest
```

Note, it is only useful for auto generated nginx config.

## Scripts
Support custom script, please see base image [docker-nginx-php](https://hub.docker.com/r/wwtg99/docker-nginx-php7).

## Author
[wwtg99](http://52jing.wang)
