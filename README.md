﻿# Примечание к форку
Более хорошая структуризация разделов и подразделов.

Немного подправлена преамбула.

*Крайне рекомендую настроить окружение из Sublime + LaTeXTools + SumatraPDF.* Будут вам и [горячие клавиши](https://latextools.readthedocs.io/en/latest/keybindings/), и предпросмотр формул и картинок, и быстрый переход из кода в pdf-ку и обратно и много всяких других фич.

Для сборки документа рекомендуется выбрать LaTeX - Basic Builder - PdfLaTeX (для отображения списка сборщиков: ctrl + shift + B, находясь в каком-либо .tex файле).

# Цель
Цель данного проекта покончить с мучениями связанными с оформлением записок к дипломным проектам в соответствии с требованиями [БГУИР](http://bsuir.by).
Способ достижения цели - создание шаблона структуры проекта для LaTeX с преамбулой, настроенной под соблюдение требований к оформлению записок.
Документ в соответствии с которым настраивается оформление документа: [СТАНДАРТ ПРЕДПРИЯТИЯ. ДИПЛОМНЫЕ ПРОЕКТЫ (РАБОТЫ). ОБЩИЕ ТРЕБОВАНИЯ СТП 01—2013](http://www.bsuir.by/m/12_100229_1_80040.pdf).


# Рекомендации
* Рекомендуемый дистрибутив LaTeX для Windows [MiKTeX](http://miktex.org/).
* Рекомендуемый редактор [Sublime](http://www.sublimetext.com/) вместе с [менеджером пакетов](http://wbond.net/sublime_packages/package_control) и установленным пакетом [LaTeXTools](https://github.com/SublimeText/LaTeXTools) и PDF просмотрщиком [SumatraPDF](http://blog.kowalczyk.info/software/sumatrapdf/free-pdf-reader.html).
* Рекомендуемые справочные пособия по вопросам связанным с LaTeX: [Bing](http://bing.com/?mkt=en-us), [Google](http://google.com), [Yandex](http://ya.ru) и книги.
* Рекомендуемая программа для ведения библиографической базы данных: [JabRef](http://jabref.sourceforge.net/)
* Инструкция по установке русского Times New Roman из пакета pscyr находится [здесь](http://plumbum-blog.blogspot.com/2010/06/miktex-28-pscyr-04d.html)
* Если возникли **проблемы с pscyr**, то можно переключиться на использование **scalable-cyrfonts-tex**, с которым также могут быть проблемы при установке, но их **проще решить** (см. 
[Wiki→Возникающие-ошибки](https://github.com/mstyura/bsuir-diploma-latex/wiki/Возникающие-ошибки#scalable-cyrfonts-tex-on-ubuntu))

## Установка
### Linux, Ubuntu (TeX Live)
- установить texlive-full: `sudo apt-get install texlive-full`
- установить модифицированный [scalable-cyrfonts-tex](https://yadi.sk/d/GW2PhDgEcJH7m): `sudo dpkg -i scalable-cyrfonts-tex-shurph_4.16_all.deb`
- можно приступать к сборке проекта

### Windows (MiKTeX)
- см. выше список рекомендаций
- раскомментировать строку `\input{FontsWindows}` в файле `preamble.tex` (и закомментировать строку `\input{FontsLinux}`)


# Примечание
Многое, наверное, сделано некрасиво и не правильно с точки зрения LaTeX, но я пока новичок и только учусь.
__Первоначальная компиляция проекта может занять некоторое время, т.к. должны установиться пакеты, используемые в Preamble.tex__.
Для диагностики неисправности рекомендуется посмотреть генерируемый log файл или запустить компиляцию из командной строки с помощью pdflatex.
