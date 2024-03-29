# Домашнее задание по курсу "Прикладной питон".

Подготовил: Тимур Ермешев

____

## Задача проекта:

Написать веб-сервис на FastAPI и развернуть его через docker.

____


## Описание сервиса:

Сервис предоставляет API производит предсказания стоимости автомобилей используя предобученную ML модель, а также запись предсказаний в базу данных.

Реализуются такие функции, как:

GET/ - проверка жизнеспособности сервиса

GET/get_cars - получение всех записей о машинах из базы

POST/predict - предсказание стоимости одной машины

POST/predict_by_csv - предсказание стоимости машин при помощи загруженного файла csv

POST/predict_by_json - предсказание стоимости машин при помощи загруженного файла json

____



## Описание параметров

**Признаки**

    name - название автомобиля
    brand - бренд автомобиля
    model - модель автомобиля
    year - год выпуска
    km_driven - показания одометра
    fuel - тип топлива
    seller_type - тип продавца (частное лицо, дилер ...)
    transmission - тип трансмиссии
    owner - владелец (первый, второй, ... )
    mileage - расход топлива
    engine - объем двигателя
    max_power - мощность
    torque - крутящий момент
    seats - количество посадочных мест

**Целевой признак**

    selling_price - стоимость автомобиля
    predicted_price - предсказанная стоимость автомобиля


____

## Запуск Docker Compose

Сборка контейнера

```bash
docker compose build --no-cache

```
Запуск контейнера

```bash
docker compose up

```
Остановка работы контейнера

```bash
docker compose down

```

## Ссылка на сервис

https://carpredict-59ah.onrender.com

## Тест

Для тестирования в директории test_files находятся подготовленные csv и json файлы для тестирования работы сервиса

