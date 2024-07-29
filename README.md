**Домашнее задание**
Построение системы централизованного логирования на основе Opensearch

**Цель:**
Cообщения сохраняются в базу Opensearch и могут быть визуализированы через Opensearch Dashboard.
В ДЗ тренируются навыки:

навыки работы с fluentbeat;
навыки работы с datapreper;
навыки работы с opensearch.

Описание/Пошаговая инструкция выполнения домашнего задания:
Возьмите за основу стенд из занятий по Elasticstack:

Замените filebeat на fluentbeat с аналогичной конфигурацией;
Замените logstash на datapreper он должен принимать данные от fluentbeat;
Замените Elasticsearch и Kibana на Opensearch и Opensearch Dashboard.


На одной машине ip 192.168.112.27 запущены в контейнерах 
Opensearch 2 ноды.
Opensearch-dashboards
Dataprapper

На другой машине ip 192.168.112.125 запущен в контейнере
fluent-bit он собиарет данные c этого же хоста где установлены ngixn(cms), mariadb, pho-fpm. Отправляет всё в data-prapper и opoensearch.

![Screenshot_6](https://github.com/user-attachments/assets/4a1ad770-9d12-4551-a4f2-c9e9490617b5)

**В opensearch добавлены индексы.**

![Screenshot_1](https://github.com/user-attachments/assets/47463209-3cbb-448d-a5a6-d4fdadab8e72)


![Screenshot_5](https://github.com/user-attachments/assets/a333d1bd-fd3a-4310-a0ae-553741bcae6c)


**Логи ngixn**


![Screenshot_4](https://github.com/user-attachments/assets/8b6bc12b-8699-4283-858c-d1afc0ccc987)


**Логи mariadb (логируем запросы)** Врятли их кончено логируют, но остальные логи полупустые ошибок нет просто.

![Screenshot_3](https://github.com/user-attachments/assets/d19e70ae-ee2c-46bd-aef7-1edea5dde83e)



**Логи php-fpm**

![Screenshot_2](https://github.com/user-attachments/assets/3a4e981c-37bc-4e59-ad61-52a2b0bd76aa)

