bachelor-diploma
================
Дипломная работа бакалавра в LaTeX, оформленная в соответствии с нормоконтролем Севастопольского государственного университета

![PDF Status](https://www.sharelatex.com/github/repos/Amet13/bachelor-diploma/builds/latest/badge.svg)

Особенности
-----------
* использование XeLaTeX, основной шрифт Times New Roman, 14pt, полуторный межстрочный интервал
* подрисуночные и подтабличные записи в формате `номерСекции.номерРисунка`
* нумерация страниц справа сверху
* возможность указания начала нумерации страниц
* возможность настройки отступов страниц
* маркировка списка символом `--`
* нумерованные списки обозначаются строчными буквами кириллицы со скобкой
* названия секций в верхнем регистре, включая содержание
* отступ в одну строку после имени заголовка
* отступы в одну строку до и после имени заголовков второго и третьего уровней
* пользовательские функции добавления рисунков, приложений и библиографии
* использование `listings` для оформления исходного кода в документе, шрифт FreeMono
* возможность добавления своих PDF в документ
* добавление библиографии в файл `0-bibliography.tex`
* чертежи и плакаты в формате А1
* бланки задания, пояснительной записки, акта внедрения
* доклад, который представляется на защите диплома
* `Makefile` для компиляции и сборки проекта

Структура исходников
--------------------
Структура каталогов:
```
.
├── extra
│   ├── drafts
│   └── posters
├── images
│   ├── infrastructure
│   ├── testing
│   └── userguide
└── inc
    └── ddos-deflate
```

В корневом каталоге `.` находится файл `main.tex`.
В `main.tex` подключается все, включая преамбулу, титульный лист, приложения и т.д.

В каталоге `extra/` находятся подключаемые PDF файлы, которые по каким-либо причинам не были сверстны в LaTeX.

В каталоге `extra/drafts/` находятся чертежи в формате А1.

В каталоге `extra/posters/` находятся плакаты в формате А1.

В каталоге `images/` находятся рисунки, схемы.

В каталоге `images/infrastructure/` находятся схемы раздела виртуальной инфраструктуры.

В каталоге `images/testing/` находятся скриншоты систем мониторинга.

В каталоге `images/userguide/` находятся скриншоты пользовательского интерфейса в приложении Б.

В каталоге `inc/` находятся файлы, которые подключаются к `main.tex`:
* файлы формата `0-*.tex` являются ненумерованными секциями (например введение, заключение, список использованной литературы)
* файлы формата `[1-9]-*.tex` являются нумерованными секциями (например постановка задчи, обзор современных методов и технологий серверной виртуализации и т.д)
* файлы формата `[a-z]-app.tex` являются файлами приложений
* файлы формата `[a-z]*.tex` не являются секциями, они подключаются для полной работы документа (например преамбула)

В каталоге `inc/ddos/` находятся файлы, взятые из репозитория: https://github.com/Amet13/ddos-deflate

Работа с LaTeX
--------------
Для работы с LaTeX рекомендую использовать XeLaTeX и IDE [LaTeXila](https://wiki.gnome.org/Apps/LaTeXila).

Как установить LaTeX: http://blog.amet13.name/2014/06/latex.html

Для пользователей GNU/Linux можно воспользоваться Makefile.
Пример компиляции проекта:
```bash
git clone https://github.com/Amet13/bachelor-diploma.git
cd bachelor-diploma/
make
```
Пример очистки ненужных файлов после компиляции:
```bash
make clean
```

Лицензия
--------
[Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](http://creativecommons.org/licenses/by-sa/4.0/deed.ru)

![CC BY SA](https://licensebuttons.net/l/by-sa/4.0/88x31.png)

Благодарности
-------------
Анатолию Смолянинову: [github.com/zarkone/bachelor](https://github.com/zarkone/bachelor)

Александру Полозову: [habrahabr.ru/post/144648](http://habrahabr.ru/post/144648/)

[Руслану Вихрову](http://defuze.cc.ua), Даниилу Велешко, [Сергею Сивкову](https://github.com/SerjSivkov) за исправление ошибок

Пользователям сайта [www.linux.org.ru](https://www.linux.org.ru/) в решении вопросов, связанных с LaTeX
