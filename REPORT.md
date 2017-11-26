Пример сериализации структуры Person
``` ShellSession
 cmake -H. -B_builds
$ cmake --build _builds
$ cd _builds
$ ./pack
```
Файл Person.yml:

``` ShellSession
first_name: Danya
last_name: Frostov
nickname: DanyaFrostov
server: ya.ru
age: 18
phone: "8(495)111-11-11"
```
Проверка валидности

``` ShellSession
$ yamllint Person.yml
Person.yml
  1:1       warning  missing document start "---"  (document-start)
```
Пример десериалиализации:
``` ShellSession
[Person]
First name: Danya
Last name: Frostov
Email: DanyaFrostov@ya.ru
Age: 18
Phone: "8(495)111-11-11"
```
