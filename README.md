# Оффлайн библиотека книг с сайта tululu.org

![image](https://drive.google.com/uc?export=view&id=1kLJZUeF5MK_3D2mKutUk7XKs47WqtNLv)
[Ссылка](https://romanulanov.github.io/pages/index1.html) на сайт.

Программа для скачивания книг в жанре научной фантастики с сайта https://tululu.org. В результате выполнения программы вы получите папку со скачанными книгами, папку с обложками книг и JSON-файл с описанием скачанных книжек. 

### Как установить

Python3 должен быть уже установлен. 
Затем используйте `pip` (или `pip3`, если есть конфликт с Python2) для установки зависимостей:
```
pip install -r requirements.txt
```

### Аргументы

Без заданных значений программа будет скачивать все книги в жанре научной фантастики (с 1 по 701 страницу). Для этого напишите в окружении просто:
```
python parse_tululu_category.py
```
Укажите в start_page (по умолчанию задано 1) с какой страницы начать скачивание книг и в end_page (по умолчанию задано 701) номер последней страницы. Например, чтобы скачать книги с 20 по 30 страницу напишите в окружении:
```
python parse_tululu_category.py --start_page 20 --end_id 30 
```
Или если хотите скачать книги с какой-либо страницы по последнюю, задайте в окружении только start_page. Например, чтобы скачать все книги с 600-ой по последнюю страницу, напишите:
```
python parse_tululu_category.py --start_page 600
```
Если не хотите скачивать обложки к книгам, напишите в запросе skip_imgs. Например, чтобы скачать только книги без обложек с 20 по 30 страницу, напишите в окружении:
```
python parse_tululu_category.py --start_page 20 --end_id 30 --skip_imgs
```
Если не хотите скачивать сами книги, напишите в запросе skip_txt:
```
python parse_tululu_category.py --skip_txt
```
Чтобы скачать книги в определённую папку, задайте полный путь к каталогу с результатами парсинга в аргументе dest_folder:
```
python parse_tululu_category.py --dest_folder E:/games
```

### Цель проекта

Код написан в образовательных целях на онлайн-курсе для веб-разработчиков [dvmn.org](https://dvmn.org/).