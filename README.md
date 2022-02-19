# Linux terminal (GitBash) commands

1) **Посмотреть где я**
`pwd`

2) **Создать папку** 
`mkdir newfolder`

3) **Зайти в папку**
`cd newfolder`

4) **Создать 3 папки**
`mkdir -p folder1 folder2 folder3`

5) **Зайти в любоую папку**
`cd folder1`

6) **Создать 5 файлов (3 txt, 2 json)** 
`touch file{1,2,3}.txt file{4,5}.json`

7) **Создать 3 папки**
`mkdir folder{1,2,3}`

8. **Вывести список содержимого папки** 
`ls`

9) **Открыть любой txt файл** 
`vim file1.txt`

10) + **написать туда что-нибудь, любой текст.**
`i` - для перехода в режим редактирования

11) + **сохранить и выйти.**
`esc` - выход из режима редактирования
`:wq`
12) **Выйти из папки на уровень выше** 
`cd ..`

13) **Переместить любые 2 файла, которые вы создали, в любую другую папку.** 
` mv folder1/file{1.txt,4.json} folder1/folder6`

14) **Скопировать любые 2 файла, которые вы создали, в любую другую папку.** 
`cp folder1/file{2,3}.txt folder1/folder4`

15) **Найти файл по имени** 
`find . -name "file1*"`

16) **Просмотреть содержимое в реальном времени.**
`tail -F ./folder1/folder6/file1.txt`
выход - `Cntr + c`

17) **Вывести несколько первых строк из текстового файла** 
`grep '' folder1/folder6/file1.txt | head -3`

18) **вывести несколько последних строк из текстового файла**
`grep '' folder1/folder6/file1.txt | tail -3`

19) **Просмотреть содержимое длинного файла (команда less) изучите как она работает.** 
`less -N longtext.txt (q - для выхода из режима просмотра)`

20) **вывести дату и время** 
`date`

----------------------
***Задание \****
1) **Отправить http запрос на сервер http://162.55.220.72:5005/terminal-hw-request**
```
curl "http://162.55.220.72:5005/terminal-hw-request"
curl "http://162.55.220.72:5005/get_method?name=(Zhanna)&age=(35)"
```

2) **Написать скрипт который выполнит автоматически пункты 3, 4, 5, 6, 7, 8, 13**
----------------------
```
touch myscript
vim myscript
i
```
***--- Текст скрипта ---***
```
#!/bin/bash
cd folderscript
mkdir -p folderscript1 folderscript2 folderscript3
cd folderscript1
touch file{1,2,3}.txt file{4,5}.json
mkdir -p folderscript{4,5,6}
ls
mv file{1,2}.txt folderscript4
```
***--- Выход из редактора ---***
```
Нажать esc
:wq
chmod +x ./myscript
./myscript
```
