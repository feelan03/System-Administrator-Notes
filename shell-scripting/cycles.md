# Циклы
## Циклы for
Пример:
```
for var in list
do
команды
done
```
Каждый повтор цикла в перменную вар будетч записывается следущиее значения из списка list
### Перебор простых значений
```
#!/bin/bash
for var in first second third fourth fifth
do
echo The  $var item
done
```
### Перебор сложных значений
```
#!/bin/bash
for var in first "the second" "the third" "I’ll do it"
do
echo "This is: $var"
done
> This is: first
> This is: the second
> ...
```
### Инициализация цикла списком, из результата команды
```
#!/bin/bash
file="myfile"
for var in $(cat $file)
do
echo " $var"
done
```
> Подобный подход, если ожидается построчная обработка данных, не сработает для файла более сложной структуры, в строках которого может содержаться по несколько слов, разделённых пробелами. Цикл будет обрабатывать отдельные слова, а не строки.


