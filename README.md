# Домашнее задание к занятию «Базы данных - Гнедин Максим»

### Инструкция по выполнению домашнего задания

1. Сделайте fork [репозитория c шаблоном решения](https://github.com/netology-code/sys-pattern-homework) к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/gitlab-hw или https://github.com/имя-вашего-репозитория/8-03-hw).
2. Выполните клонирование этого репозитория к себе на ПК с помощью команды `git clone`.
3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
   - впишите вверху название занятия и ваши фамилию и имя;
   - в каждом задании добавьте решение в требуемом виде: текст/код/скриншоты/ссылка;
   - для корректного добавления скриншотов воспользуйтесь инструкцией [«Как вставить скриншот в шаблон с решением»](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md);
   - при оформлении используйте возможности языка разметки md. Коротко об этом можно посмотреть в [инструкции по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md).
4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`).
5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
6. Любые вопросы задавайте в чате учебной группы и/или в разделе «Вопросы по заданию» в личном кабинете.

Желаем успехов в выполнении домашнего задания.

---
### Легенда

Заказчик передал вам [файл в формате Excel](https://github.com/netology-code/sdb-homeworks/blob/main/resources/hw-12-1.xlsx), в котором сформирован отчёт. 

На основе этого отчёта нужно выполнить следующие задания.

### Задание 1

Опишите не менее семи таблиц, из которых состоит база данных:

- какие данные хранятся в этих таблицах;
- какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.

Приведите решение к следующему виду:

Сотрудники (

- идентификатор, первичный ключ, serial,
- фамилия varchar(50),
- ...
- идентификатор структурного подразделения, внешний ключ, integer).

### Решение:

Сотрудники (  
идентификатор, первичный ключ, serial,  
фамилия varchar(50),  
имя varchar(50),  
отчество varchar(50),  
Оклад money,  
Идентификатор должности, внешний ключ, serial  
Идентификатор типа подразделения, внешний ключ, serial  
Идентификатор подразделения, внешний ключ, serial  
Дата найма date,  
Идентификатор города филиала, внешний ключ, serial  
Идентификатор адреса филиала, внешний ключ, serial  
)  
  
Должности (  
Идентификатор, serial  
Название должности varchar(100),  
)  
  
Типы подразделений (  
Идентификатор, serial  
Тип подразделения varchar(40),  
)  
Города филиалов (  
Идентификатор, serial  
Город филиала varchar(50)  
)  
Адреса филиатлов (  
Идентификатор, serial  
Адрес филиала varchar(150)  
)  
  
Проекты (  
Идентификатор, serial  
Название проекта varchar(100),  
)  

Структурные подразделения (  
Идентификатор подразделения serial,  
Название подразделения varchar(100)  
)  
  
Назначения на проекты (  
Идентификатор сотрудника serial,  
Идентификатор проекта serial   
)


## Дополнительные задания (со звёздочкой*)
Эти задания дополнительные, то есть не обязательные к выполнению, и никак не повлияют на получение вами зачёта по этому домашнему заданию. Вы можете их выполнить, если хотите глубже шире разобраться в материале.


### Задание 2*

Перечислите, какие, на ваш взгляд, в этой денормализованной таблице встречаются функциональные зависимости и какие правила вывода нужно применить, чтобы нормализовать данные.
