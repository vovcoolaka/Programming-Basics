# Класс
Описание свойств (атрибутов) и методов (взаимодействия) какой-либо сущности.
#### Например:
    Класс: Летательные аппараты
    Свойства: вес, дальность полета, тип топлива, скорость
    Методы: запуск двигателя, ускорение, взлет, посадка, набор высоты, снижение

# Объект 
Cущность описанная в классе.

    Например, объекты класса летательные аппараты:
- Возлушный шар, 
- самолет, 
- вертолет,
- автожир, 
- ракета, 
- дирижабль

# Абстракция
Имеет множество уровней, необходима для создания "универсальных классов".
Нет смысла создавать отдельные классы для каждого объекта, абстракция позволяет объединять/группировать объекты и сосредотачиваться на их основных свойствах, позволяет подниматься на уровень (или несколько) выше и описывать в одном классе нужное нам количество объектов.

    Пример: АН-2 (кукурузник) - одномоторные самолеты - самолеты с винтовым    
    двигателем - самолеты - летательные аппараты

# Наследование
Позволяет создать новый класс на основе уже существующего.
Если класс не содержит необходимые свойства или методы, используется наследование, класс-потомок наследует все свойства и методы класса-родителя и дополняется новыми.

    Пример: Класс-родитель - летательные аппараты, класс-потомок самолеты
    новые свойства: размах крыла, количетсво двигателей, количество пассажиров

# Полиморфизм
    Один и тот же интерфейс для разных объектов класса.
    Например: Каждый объект класса летательные аппараты имеет метод взлет, но в каждом случае он осущетсвляется по-разному.

# Инкапсуляция

    Скрывает принципы работы метода, то есть Вы можете использовать метод не зная его внутреннее устройство. Для запуска двигателя любого летательного оператора не нужно знать всех подробностей - как подается топливо, как оно воспламеняется и т. п.

# SOLID
Следование принципам SOLID позволяет писать легкочитаемый и легкоподдерживаемый код.

- S - У нас есть самолет для перевозки пассажиров, если нужен самолет для тушения пожаров мы делаем новую модель беря за основу пассажирский
- О - Самолет можно расширить, добавить двигатель или оборудование, но модифицировать в вертолет нельзя
- L - Техники заправляющие самолет могут заправить любой самолет
- I - Для управления самолетом и его обслуживания используются разные интерфейсы, а не один универсальный для всех
- D - К примеру на основании пассажирского самолета создали грузовой самолет, первый никак не зависит от второго, но оба зависят от абстракции летательные аппараты, от которой в свою очередь зависят детали реализации (должны быть крылья  и т. п.)