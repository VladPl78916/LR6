# LR6
Лабораторная работа №6

# Отчет по лабораторной работе №6
## Тема: Система контроля версий

## Цель лабораторной работы
Изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и
удаленным репозиторием. 

## Порядок выполнения работы
В ходе выполнения работы были выполнены следующие шаги:

### Шаг 1: Создание аккаунта на GitHub
Зарегистрирован аккаунт на сайте GitHub.

### Шаг 2: Форк репозитория
Форкнут репозиторий с заданием: [https://github.com/Kurtyanik/LR6](https://github.com/Kurtyanik/LR6).

![Скриншот форка репозитория](photo/fork.jpg)

### Шаг 3: Установка Git
Установлен Git с сайта [https://git-scm.com/](https://git-scm.com/).

### Шаг 4: Настройка Git
Настроен клиент Git с помощью следующих команд:

```bash
git config --global user.name "Группа Фамилия И.О."
git config --global user.email "ваш_емейл@example.com"
```
![Скриншот настройки клиента](photo/name_email.jpg)

### Шаг 5: Клонирование репозитория

```bash
git clone https://github.com/Kurtyanik/LR6
```
![Скриншот клонирования репозитория](photo/clone.jpg)

### Шаг 6: Добавление файла через GitHub и подтягивание изменений
Добавлен файл через веб-интерфейс GitHub и изменения подтянуты локально:

```bash
git pull
```
![Скриншот добавления файла](photo/add_pull_file.jpg)

### Шаг 7: Получение истории операций
Получена история операций для каждой ветки:

```bash
git log --oneline --all
```
![Скриншот истории операций для каждой ветки](photo/history_commits.jpg)

### Шаг 8: Просмотр последних изменений
Посмотрены последние изменения:

```bash
git log -p -1
```
![Скриншот просмотра последних изменений](photo/last_commit.jpg)

### Шаг 9: Слияние ветки и разрешение конфликта
Создана и слита ветка feature в master, конфликтов не возникло:

```bash
git checkout -b feature
# Внесены изменения
git add .
git commit -m "Внес изменения в feature"
git checkout master
git merge feature
```
![Скриншот слияния веток](photo/merge.jpg)

### Шаг 10: Удаление побочной ветки
Удалена ветка feature после слияния:

```bash
git branch -d feature
```

### Шаг 11: Сделаны несколько коммитов с комментариями
Внесены изменения в файл example.txt (поочерёдно добавил две строки) и сделаны коммиты:

```bash
git add example.txt
git commit -m "Добавлена новая строка в файл example.txt"
git add example.txt
git commit -m "Добавил ещё одну строку(второй коммит).txt"
```
![Скриншот создания коммитов](photo/commits.jpg)

### Шаг 12: Откат коммита
Выполнен откат последнего коммита:

```bash
git add example.txt
git commit -m "Добавлена новая строка в файл example.txt"
git add example.txt
git commit -m "Добавил ещё одну строку(второй коммит).txt"
```
![Скриншот отката коммита](photo/otkat_commit.jpg)


### Шаг 13: Создание ветки для отчета
Создана ветка report для оформления отчета:

```bash
git branch report
git checkout report
```
![Скриншот создания ветки для отчёта](photo/report_branch.jpg)

## Лог команд

```bash
# Настройка имени пользователя и email
git config --global user.name "4314 Плюснин В.Д."
git config --global user.email "vpd658@mail.ru"

# Клонирование форкнутого репозитория
git clone https://github.com/Kurtyanik/LR6

# Переключение в директорию проекта
cd LR6

# Получение истории операций для всех веток
git log --oneline --all

# Просмотр последних изменений
git log -p -1

# Создание новой ветки
git branch feature

# Переключение на новую ветку
git checkout feature

# Внесение изменений, добавление их в индекс и коммит
git add example.txt
git commit -m "Добавил новую строку в example.txt"

# Переключение обратно на мастер и слияние веток
git checkout master
git merge feature

# Удаление побочной ветки после слияния
git branch -d feature

# Создание еще нескольких коммитов с комментариями
git add example.txt
git commit -m "Добавлена новая строка в файл example.txt"
git add example.txt
git commit -m "Добавил ещё одну строку(второй коммит).txt"

# Откат последнего коммита
git revert HEAD

# Создание ветки для отчета и переключение на нее
git branch report
git checkout report

# Получение истории операций в отформатированном виде
git log --pretty=format:"%h %ad | %s%d [%an]" --date=short

# Отправка изменений на удаленный репозиторий
git push origin report
```

### Пояснение:
Этот лог команд показывает весь процесс выполнения лабораторной работы, включая настройку Git, создание веток, коммиты, слияние, откат коммитов и отправку изменений на GitHub.


