# task-1-OOP-basics
### Написать реализацию класса транспортное средство `Vehicle`. Класс необходимо создавать в отдельном файле (модуле) и импортировать в файл `main.py`. После чего в файле `main.py` создать экземпляры (объекты) этого класса и убедиться в том, что реализованный функционал работает правильно.
## Пример директорий для данного задания
```
task-1-OOP-basics
    ├──src
    │    ├──Vehicle.py
    │    ├──main.py
    ├──TASK.md
```
## Описание класса `Vehicle`
### Конструктор данного класса должен принимать следующие аргументы и устанавливать соответствующим приватным атрибутам значения этих аргументов:
`__init__(model_name, engine_power, color, manufacture_year, manufacture_country, doors_сount, hijacked_status)`
### У класса `Vehicle` должны быть следующие приватные атрибуты:
Название атрибута | Описание атрибута | Тип данных
------------------|-------------------|--------------
`__model_name` | Название модели | `str`
`__engine_power` | Мощность двигателя | `int`
`__color` | Цвет | `str`
`__manufacture_year` | Год выпуска | `int`
`__manufacture_country` | Страна-производитель | `str`
`__doors_сount` | Количество дверей | `int`
`__hijacked_status` | Если т/с в угоне - данный атрибут принимает значение `true`, иначе - `false` | `bool`
`__engine_status` | Если двигатель т/с заведен - данный атрибут принимает значение `true`, иначе - `false` | `bool`
`__headlights_status` | Если фары т/с включены - данный атрибут принимает значение `true`, иначе - `false` | `bool`
### Для того, чтобы пользователь мог получить информацию о транспортном средстве, необходимо создать одноименные с атрибутами свойства-геттеры:
Название свойства | Что должно возвращаться пользователю, при обращении к данному свойству
------------------|-----------------------------------------------------------------------
`model_name` | Строку, содержащую название модели
`engine_power` | Число, означающее мощность двигателя
`color` | Строку, содержащую цвет транспортного средства
`manufacture_year` | Число, означающее год выпуска т/с
`manufacture_country` | Строку, содержащую страну-производителя
`doors_сount` | Число, означающее количество дверей в т/с
`hijacked_status` | Если т/с в угоне, необходимо вернуть строку `Данное т/с в угоне!`. Если нет - то строку `Данное т/с не имеет криминальной истории`
`engine_status` | Если двигатель запущен, необходимо вернуть строку `Двигатель запущен`. Если нет - то строку `Автомобиль не заведен`.
`headlights_status` | Если фары включены, необходимо вернуть строку `Фары включены`. Если нет - то строку `Фары отключены`.
### Также данный класс должен иметь следующие методы:
Название метода | Принимаемые аргументы | Описание работы
----------------|-----------------------|-----------------------------
`start_engine` | Нет | Метод запуска двигателя. Метод должен выводить в консоль строку `Двигатель запущен`. Также метод должен менять статус двигателя в атрибуте `__engine_status` на `true`.
`stop_engine` | Нет | Метод отключения двигателя. Метод должен выводить в консоль строку Двигатель остановлен. Также метод должен менять статус двигателя в атрибуте `__engine_status` на `false`.
`switch_on_headlights` | `light_type`:`str` - режим освещения. Для аргумента возможны только два значения: `"ближний"` и `"дальний"` | Метод включения фар. В зависимости от принимаемого аргумента включается ближний или дальний свет фар. В методе необходимо предусмотреть проверку на корректность аргумента `light_type` и в случае ошибки вывести в консоль строку `Вы выбрали неверный режим освещения. Возможные режимы: "ближний" и "дальний"`. Если аргумент корректен, то в зависимости от аргумента вывести либо строку `Включен ближний свет`, либо строку `Включен дальний свет`. Также метод должен менять статус освещения в атрибуте `__headlights_status` на `true`.
`switch_off_headlights` | Нет | Метод для отключения фар. Должен выводить в консоль строку `Фары отключены`. Также метод должен менять статус освещения в атрибуте `__headlights_status` на `false`.
### Список источников, которые могут помочь в реализации данного задания
+ [https://metanit.com/python/tutorial/7.1.php](https://metanit.com/python/tutorial/7.1.php)
+ [http://python-3.ru/page/svojstva-klassa-oop-python](http://python-3.ru/page/svojstva-klassa-oop-python)
+ [https://younglinux.info/oopython.php](https://younglinux.info/oopython.php)
+ [https://python-scripts.com/object-oriented-programming-in-python](https://python-scripts.com/object-oriented-programming-in-python)
