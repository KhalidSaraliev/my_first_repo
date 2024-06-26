# Работа с  удаленной репозиторией: 

Чтобы скопировать удаленный репозиторий нужно открыть страницу и нажать на 
```sh
Code
```
И скопировать от туда ссылку. В терминале пишем 
```sh
git clone <ссылка репозитория>
```
Чтобы удостоверится появилась нужна директория можно набрать команду
```sh
ls
```
Потом нужно войти в папку с данной репозиторией набрав команду
```sh
cd <имя_папки>
```
Команда чтобы посмотреть какие комиты были созданы в репозитории:
```sh
git log --oneline
```

Команда для визуализации веток которые были или есть в репозитории:
```sh
git log --graph
``` 

Чтобы выйти из просмотра веток нужно нажать:

```sh
q
```

Для работы на Github нужно зарегистроваться на сайте и создаем свою первую репозиторию **НО ВАЖНО** знать что недоспутимы проблемы в названии репозитория.
Чтобы связать удаленку нужно следовать указаниям на сайте:
1. Создать файл с желаемым названием
2. Инициализировать локальный репозиторий командой 
```
git init
``` 
Потом фиксируем файл командой
```sh
git add <название_файла>
```
Потом пишем коммит, команда:
```sh
git commit -m "коммит"
```
Если ветка называется не "MAIN" то переименуем командой:
```sh
git branch -M main
```
3. Указываем в качестве удаленного репозитория по умолчанию ставив ссылку созданного нами репозитория на сайте:
```sh
git remote add origin <ссылка нашего репозитория>
```
Теперь мы связали удаленный репозиторий с локальным, настроили связь. И теперь наша задача вытолкнуть на сервер переделанный файл. Для этого нужно набрать команду:
```sh
git push -u origin main
```

Это текст добавлен с веб сервера

Добавил текст  локально

Добавил текст в новой ветке

Чтобы вытолкнуть на сервер новую добавленную ветку нужно набрать команду:
```sh
git push --set-upstream origin newbranch
```
Разрешаю конфликт по новой
