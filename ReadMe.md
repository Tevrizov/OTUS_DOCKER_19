# Docker
Цель домашнего задания
Разобраться с основами docker, с образом, эко системой docker в целом;



### 1.Создать свой кастомный образ nginx на базе alpine. 
После запуска nginx должен отдавать кастомную страницу (достаточно изменить дефолтную страницу nginx).






### 2.Определить разницу между контейнером и образом.


__Контейнер__ 
    При запуске контейнерной среды внутри контейнера создается копия файловой системы (docker образа) для чтения и записи.
    Контейнер Docker (Docker Container) - это виртуализированная среда выполнения, в которой пользователи могут изолировать 
    приложения от хостовой системы. Эти контейнеры представляют собой компактные портативные хосты, в которых можно быстро 
    и легко запустить приложение.
    Контейнеры работают автономно, изолированно от основной системы и других контейнеров, и потому ошибка в одном из них 
    не влияет на другие работающие контейнеры, а также поддерживающий их сервер.



__Образ__ 
    Образ Docker (Docker Image) - это неизменяемый файл, содержащий исходный код, библиотеки, зависимости,
    инструменты и другие файлы, необходимые для запуска приложения.
    Образы предназначены только для чтения их иногда называют снимками (snapshot).
    Они представляют приложение и его виртуальную среду в определенный момент времени. 
    Так как образы являются просто шаблонами, их нельзя создавать или запускать. 
    Этот шаблон можно использовать в качестве основы для построения контейнера
    Образ - это шаблон, на основе которого создается контейнер, существует отдельно и не может быть изменен.
    Образ собирается из:
        слоев, каждый слой собирается из своей директивы в Dockerfile'е, где директивы ENV и ARG не являются слоями и
        начального образа, болванки, из директивы FROM в Dockerfile'е.
    Таким образом, образы могут состоять из ряда слоев, каждый из которых отличается от предыдущего.
    Слои образа представляют файлы, доступные только для чтения, поверх которых при создании контейнера добавляется новый слой.
    Можно создать/запустить неограниченное количество контейнеров из одного образа.
    


__Отличие от виртуализации__
    В отличие от виртуальных машин, где виртуализация выполняется на аппаратном уровне,
    контейнеры виртуализируются на уровне приложений. Они могут использовать одну машину, 
    совместно использовать ее ядро и виртуализировать операционную систему для выполнения 
    изолированных процессов. Это делает контейнеры чрезвычайно легкими, позволяя сохранять ценные ресурсы.



### 3. Можно ли в контейнере собрать ядро?



### 4.Собранный образ запушить в docker hub.





Задание со звездочкой

1.Написать Docker-compose для приложения Redmine, с использованием опции build.
2.Добавить в базовый образ redmine любую кастомную тему оформления.
3.Убедиться что после сборки новая тема доступна в настройках.
4.Настроить вольюмы, для сохранения всей необходимой информации