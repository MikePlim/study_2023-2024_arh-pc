	---
## Front matter
title: "Отчёт по лабораторной работе №6"
subtitle: "Простейший вариант"
author: "Янушкевич Михаил Денисович"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Содержание
1. Цель работы
2. Выполнение лабораторной работы
3. Задание для самостоятельной работы
4. Вывод

# Цель работы

Освоение арифметических инструкций языка ассемблера NASM.

# Выполнение лабораторной работы
1. Создать каталог для программ лабораторной работы №6, в нём создать файл lab6-1.asm.(рис. @fig:001).

![1](image/1.png){#fig:001 width=70%}

С помощью команды mkdir создаём каталог lab06, далее в нём, с помощью команды touch создаём файл lab6-1.asm.

2. В файл lab6-1.asm ввести текст программы из листинга 6.1.(рис. @fig:002).

![2](image/2.png){#fig:002 width=70%}

Открываем файл lab6-1.asm в редакторе gedit, вводим необходимый текст из листинга 6.1.

3. Создать исполняемый файл и запустить его.((рис. @fig:003).

![3](image/3.png){#fig:003 width=70%}

В командной строке вводим необходимые команды, чтобы создать из текстового файла исполняемый, далее запускаем его. Результатом выполения программы становится символ "j".

4. Изменить текст программы, заменяя символы регистрами чисел.(рис. @fig:004).(рис. @fig:005).

![4](image/4.png){#fig:004 width=70%}

![5](image/5.png){#fig:005 width=70%}

Текст из листинга 6.1 изменяем, заменяя необходимые строки. Далее создаём исполняемый файл,запускаем файл. Результат работы программы не выводится на экран. Опираясь на таблицу ASCII, можно понять, что код 10 соответсвует символу "пробел", который и является результатом выполнения программы.

5. Создать файл lab6-2.asm.и ввести в него текст программы из листинга 6.2.(рис. @fig:006).(рис. @fig:007).

![6](image/6.png){#fig:006 width=70%}

![7](image/7.png){#fig:007 width=70%}

В каталоге lab06 создаём файл lab6-2.asm и вводим в него текст программы из листинга 6.2.

6. Создать исполняемый файл и запустить его.(рис. @fig:008).

![8](image/8.png){#fig:008 width=70%}

В командной строке вводим необходимые команды, чтобы создать исполняемый файл. Далее запускаем его. Результатом работы программы будет число 106.

7. Заменить необходимые строки в тексте листинга 6.2. Создать исполняемый файл и запустить его.(рис. @fig:009).(рис. @fig:010).

![9](image/9.png){#fig:009 width=70%}

![10](image/10.png){#fig:010 width=70%}

В тексте файла lab6-2.asm заменяем необходимые строки. Далее создаём исполняемый файл, запускаем его. Как можно увидеть, результатом работы программы будет число 10.

8. В тексте файла lab6-2.asm заменить функцию iprintLF на iprint.(рис. @fig:011).(рис. @fig:012).

![11](image/11.png){#fig:001 width=70%}

![12](image/12.png){#fig:001 width=70%}

В файле lab6-2.asm заменяем функцию iprintLF на iprint. Создаём исполняемый файл и запускаем программу. Результатом выполнения программы будет число 10. В отличие от вывода функции iprintLF, iprint выводит результат в одну строчку.

9. Создать файл lab6-3.asm в каталоге lab06. В файл ввести текст программы из листинга 6.3. Создать исполняемый файл и запустить его.(рис. @fig:013).(рис. @fig:014).(рис. @fig:015).

![13](image/13.png){#fig:013 width=70%}

![14](image/14.png){#fig:014 width=70%}

![15](image/15.png){#fig:015 width=70%}

С помощью команды touch создаём файл lab6-3.asm. Открываем его и вводим текст из листинга 6.3. Создаём исполняемый файл и запускаем программу. Результатом работы программы будет число 4, а остаток будет равняться 1.

10. Изменить текст программы из файла lab6-3.asm для вычисления выражения 𝑓(𝑥) = (4 ∗ 6 + 2)/5. (рис. @fig:016).(рис. @fig:017).

![16](image/16.png){#fig:016 width=70%}

![17](image/17.png){#fig:017 width=70%}

В файле lab6-3.asm вносим необходимые изменения, чтобы вычислить выражение 𝑓(𝑥) = (4 ∗ 6 + 2)/5. Далее создаём исполняемый файл, проверяем его работу. Результатом исполнения программы будет число 5, а в остатке будет 1.

11. Создать файл variant.asm в каталоге lab06. В этот файл ввести текст программы из листинга 6.4. Создать исполняемый файл программы и запустить его.(рис. @fig:018).(рис. @fig:019).(рис. @fig:020).

![18](image/18.png){#fig:018 width=70%}

![19](image/19.png){#fig:019 width=70%}

![20](image/20.png){#fig:020 width=70%}

С помощью команды touch создаём файл variant.asm в каталоге lab06. Открываем этот файл и вводим в него текст из листинга 6.4. Эта программа вычисляет вариант задания по номеру студенческого билета. Далее запускам программу, вводим номер ст.билета(мой номер-1132231840). В результате выводится число 1, что означает, что мне достался вариант №1.

# Ответы на вопросы

1. Строки, отвечающие за вывод на экран сообщения "Ваш вариант:" mov eax,rem,  call sprint.

2. Эти конструкции используются для ввода сообщения с клавиатуры. В eax записывается адрес переменной, в которую сообщение будет записано, в edx указывается длина вводимой строки.

3. Call atoi используется для преобразования ASCII чисел в целые числа.

4. mov eax,x    - Строки, отвечающие за вычисление варианта.
   call atoi
   xor edx,edx 
   mov ebx,20
   div ebx
   inc edx
   
5. Остаток записывается в регистр edx.

6. Эта функция считывает значение eax, прибавляет к нему 1, а потом перезаписывает обратно в eax.

7. mov eax,edx    - Строки, отвечающие за вывод результата вычислений.
   call iprintLF
   

# Задание для самостоятельной работы

1. Создать файл в формате asm. В нём написать программу вычисления выражения y=f(x). Вид функции соответствует номеру варианта из предыдущего задания лабораторной работы.(рис. @fig:021).(рис. @fig:022).

![21](image/21.png){#fig:021 width=70%}

![22](image/22.png){#fig:022 width=70%}

Создаём файл variant1.asm, с помощью midnight commander убеждаемся в его создании. Далее открываем его и на основе полученных ранее знаниях пишем программу, которая будет вычислять выражение y=(10+2x)/3, где х1=1, х2=10. 

2. Запустить написанную программу и проверить её работу.(рис. @fig:023).

![23](image/23.png){#fig:023 width=70%}

После написания программы создаём объектный файл, запускаем программу. Для этого поочерёдно вводим в строку значения х. Ответами являются числа 4 и 10, из чего можно сделать вывод, что программа написана верно. 


# Выводы

Благодаря этой лабораторной работе я освоил арифметические инструкции языка ассемблера NASM, что позволило мне написать полноценную программу по вычислению выражения типа y=f(x). Также я закрепил полученные ранее навыки по работе с командной строкой ОС Linux и языком ассемблера NASM.

::: {#refs}
:::
