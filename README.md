# Домашнее задание к занятию "11.02 Микросервисы: принципы"

Вы работаете в крупной компанию, которая строит систему на основе микросервисной архитектуры.
Вам как DevOps специалисту необходимо выдвинуть предложение по организации инфраструктуры, для разработки и эксплуатации.

## Задача 1: API Gateway 

Я бы внёс предложение внедрить Nginx в качестве балансировщика. В настоящее время на Nginx размещено 34% всех сайтов в интернете, что несомненно делает его одним из самых популярных веб-серверов в мире. Также предложил Kong как масштабируемое решение, реализующее слой API Gateway. 
Kong или Kong API Gateway - это облачный, не зависящий от платформы масштабируемый API-шлюз, отличающийся высокой производительностью и расширяемостью с помощью плагинов. Предоставляя функциональность для проксирования, маршрутизации, балансировки нагрузки, проверки работоспособности, аутентификации (и многого другого).Kong служит центральным уровнем для простого управления микросервисами или обычным трафиком API.


## Задача 2: Брокер сообщений

| Параметр\Брокер | RabbitMQ | Apache Kafka | ActiveMQ | WebSphereMQ | 
|---|---|---|---|---|
| Поддержка кластеризации | + | + | + | + | 
| Хранение сообщений в процессе доставки | + | + | + | + | 
| Высокая скорость | - | + | - | + | 
| Поддержка различных форматов | + | + | - | + | 
| Разделение прав доступа | + | + | + | + |
| Простота эксплуатации | - | + | + | + | 

Основываясь на сравнении брокеров сообщений, было бы целесообразно выбрать Kafka, так как у него наибольшее количество приемуществ:
1. Гибридный характер. Kafka — это гибрид распределённой базы данных и брокера сообщений с возможностью горизонтального масштабирования. 
2. Ведение журнала событий. Kafka сохраняет данные в строго структурированной форме, в которой всегда можно отследить, когда произошло то или иное событие. 
3. Отказоустойчивость и высокая доступность. Сообщения хранятся на различных узлах-брокерах, что обеспечивает высокую доступность. 
4. Apache Kafka используется в различных направлениях IT-индустрии, от сервисов потоковых видео до аналитики Big Data. 
