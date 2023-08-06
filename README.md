# Домашнее задание к занятию 2 «Кластеризация и балансировка нагрузки» - `Антипов Николай`
### Цель задания
В результате выполнения этого задания вы научитесь:

Настраивать балансировку с помощью HAProxy
Настраивать связку HAProxy + Nginx

### Задание 1
Запустите два simple python сервера на своей виртуальной машине на разных портах
Установите и настройте HAProxy, воспользуйтесь материалами к лекции по ссылке
Настройте балансировку Round-robin на 4 уровне.
На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy.


Скриншот перенаправления запросов

![1screen](https://github.com/NikolayAntipov/dz_haproxy/blob/main/img/1screen.JPG)

Конфигурационный файл haproxy1
[1_haproxy](https://github.com/NikolayAntipov/dz_haproxy/blob/main/img/1_haproxy.cfg)



### Задание 2
Запустите три simple python сервера на своей виртуальной машине на разных портах
Настройте балансировку Weighted Round Robin на 7 уровне, чтобы первый сервер имел вес 2, второй - 3, а третий - 4
HAproxy должен балансировать только тот http-трафик, который адресован домену example.local
На проверку направьте конфигурационный файл haproxy, скриншоты, где видно перенаправление запросов на разные серверы при обращении к HAProxy c использованием домена example.local и без него.

Скриншот после установки весов серверов

![2веса](https://github.com/NikolayAntipov/dz_haproxy/blob/main/img/2weight.JPG)

Скришот отправки на другое имя отличное от example.local

![2другое имя](https://github.com/NikolayAntipov/dz_haproxy/blob/main/img/2diffname.JPG)

Конфигурационный файл haproxy2
[2_haproxy](https://github.com/NikolayAntipov/dz_haproxy/blob/main/img/2_haproxy.cfg)
