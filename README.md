# Домашнее задание к занятию «Обзор систем IT-мониторинга» - Савельев Алексей SYS-25

Что нужно сделать:
Процесс выполнения
1. В окне браузера откройте облачную платформу Yandex Cloud
2. Перейдите в раздел "Все сервисы" > "Инфраструктура и сеть" > "Compute Cloud"
3. Нажмите на синюю кнопку "Создать ВМ" в правом верхнем углу окна браузера
4. Задайте имя виртуальной машины. Используйте английские буквы и цифры.
5. Выберите операционную систему Debian 11
6. Установите объём HDD равный 3ГБ
7. Выберите платформу Intel Ice Lake
8. Установите количество vCPU равное 2
9. Установите гарантированную долю vCPU равную 20%
10. Задайте количество RAM равное 1ГБ
11. Поставьте галочку "Прерываемая"
12. В разделе "Доступ" выберите сервисный аккаунт с ролью monitoring.editor. Если такого аккаунта нету, нажмите на кнопку "Создать новый". Задайте имя аккаунта английскими буквами, напротив надписи "Роли в каталоге" нажмите на знак "плюс". Прокручивая колесо мыши на себя, найдите роль monitoring.editor и нажмите на неё левой кнопкой мыши. Теперь вы сможете найти только что созданную роль в выпадающем списке аккаунтов.
13. Задайте логин учётной записи вашей виртуальной машины
14. Вставьте публичный SHH-ключ в поле SSH-ключ. Если этого ключа у вас нету, создайте его с помощью утилиты PuTTYgen
15. Поставьте галочку "Установить" в пункте "Агент сбора метрик"
16. Нажмите на синюю кнопку "Создать ВМ"
17. Перейдите в раздел "Все сервисы" > "Инфраструктура и сеть" > "Monitoring"
18. Нажмите на кнопку "Создать дашборд", расположенную в разделе "Возможности сервиса" > "Дашборды"
19. В открывшемся окне в разделе "Добавить виджет" нажмите на "График"
20. Пред вам предстанет конструктор запросов, выберите "Запрос А"
21. В параметре service конструктора запросов выберите Compute Cloud
22. В появившемся параметре name конструктора запросов выберите cpu_utilization
23. Поправьте диапазон времени отрисовки графика нажав на кнопку "Сейчас" в верху экрана, левее кнопок 3m, 1h, 1d, 1w, "Отменить".
24. Нажмите на кнопку "Сохранить" в правом верхнем углу экрана
25. Задайте имя дашборда, если появится окно ввода имени дашборда
26. Сделайте скриншот

---

### Задание 1

1. В окне браузера открыл облачную платформу Yandex Cloud и перешёл в раздел "Все сервисы" > "Инфраструктура и сеть" > "Compute Cloud" > "Виртуальные машины" и нажал на кнопку "Создать ВМ"

![скриншот](https://github.com/Lexacbr/ya-monitoring/blob/master/screenshots/vm-create.png)

2.  Задайте имя виртуальной машины. Использовал английские буквы и цифры. Выберал операционную систему Debian 11. Установил объём HDD равный 3ГБ. Выбрал платформу Intel Ice Lake. Установил количество vCPU равное 2. Установил гарантированную долю vCPU равную 20%. Задал количество RAM равное 1ГБ. Поставил галочку "Прерываемая"

![скриншот](https://github.com/Lexacbr/ya-monitoring/blob/master/screenshots/cpu-choise.png)
 
3. В разделе "Доступ" выбрал сервисный аккаунт с ролью monitoring.editor. Задал логин учётной записи виртуальной машины. Вставил публичный SHH-ключ в поле SSH-ключ. Поставил галочку "Установить" в пункте "Агент сбора метрик". Нажал на синюю кнопку "Создать ВМ"  

![скриншот](https://github.com/Lexacbr/ya-monitoring/blob/master/screenshots/acsess.png)

4. Перешёл в раздел "Все сервисы" > "Инфраструктура и сеть" > "Monitoring". Нажал на кнопку "Создать дашборд", расположенную в разделе "Возможности сервиса" > "Дашборды". В открывшемся окне в разделе "Добавить виджет" нажал на "График". Перед мной предстал конструктор запросов, выбрал "Запрос А". В параметре service конструктора запросов выбрал Compute Cloud. В появившемся параметре name конструктора запросов выбрал cpu_utilization. Поправил диапазон времени отрисовки графика нажав на кнопку "Сейчас" в верху экрана, левее кнопок 3m, 1h, 1d, 1w, "Отменить". Нажал на кнопку "Сохранить" в правом верхнем углу экрана.Задал имя дашборда "CPU_Util". Сделал скриншот

![скриншот](https://github.com/Lexacbr/ya-monitoring/blob/master/screenshots/dash-cho.png)

![скриншот](https://github.com/Lexacbr/ya-monitoring/blob/master/screenshots/dash-end.png)

---

### Задание 2*
Чо нужно сделать:


Это дополнительное задание. Его можно не выполнять. Это не повлияет на зачёт. Вы можете его выполнить, если хотите глубже разобраться в материале.

С помощью Yandex Monitoring сделайте 2 алерта на загрузку процессора: WARN и ALARM. Создайте уведомление по e-mail.

Требования к результату
прикрепите в файл README.md скриншот уведомления в Yandex Monitoring

Что делал я:
Собственно говоря делал то, что описано в задании. В итоге получил вот такой результат:

![скриншот](https://github.com/Lexacbr/ya-monitoring/blob/master/screenshots/dash.png)

![скриншот](https://github.com/Lexacbr/ya-monitoring/blob/master/screenshots/email.png)
