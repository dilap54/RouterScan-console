# Описание
Это консольная версия программы Router Scan для linux. Она использует закрытую библиотеку Router Core Library. 
Сайт оригинала находится вот тут [http://stascorp.com/load/1-1-0-56](http://stascorp.com/load/1-1-0-56)
### Пользоваться вот так
```bash
    cat /path/to/file/with/<ip>:<port>list | ./routerscan > /results/file
```
Ключ `-d` включает вывод логов в stderr
Ключ `-t 100` Задает 100 потоков для rsscan
### Техническая часть
Файл routerscan, написанный на golang, запускает кучу файлов rsscan, который написан на Delphi, и общается с ними через stdio. rsscan динамически подключает библиотеку liblibrouter.so, которая написана на Delphi, в которой находится весь функционал по тестированию роутеров, исходный код которой закрыт и принадлежит Stas'M и которого у меня нет.