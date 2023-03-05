# Описание проекта 'Дашборд продаж для Wildberries'

## Техническое задание
1. Создать дашборд в DataLens, который будет отвечать на вопросы:
 - С какими товарами проблема (продажи идут плохо).
 - Какие товары пора поставить на склад (продажи идут хорошо).
 - На какой именно склад стоит привезти товар.
2. Собирать и хранить историю остатков на складах за последние 90 дней.

## Инструменты и навыки
DataLens, SQL, обработка и визуализация данных

## Результаты работы
Подготовлен дашборд, который включает следующие графики и таблицы: 
 - Динамика заказов - содержит информацию о количестве заказов и скользящем среднем количества заказов по дням. Даты можно группировать по периодам, для расчета скользящего среднего можно установить нижнее и верхнее значение, по умолчанию границы окон равны 1. 
 - Распределение подтверждённых заказов и возвратов по артикулу - данные отсортированы по количеству заказов в порядке убывания, что позволяет наглядно выделить товары с наибольшим и наименьшим числом заказов.
 - Распределение заказов по категориям и товарам - показывает количество заказов по группам в абсолютных и относительных значениях.
 - Распределение товаров по складам на текущую дату - даёт информацию об объёме товара по складам на сегодняшний день. 
 - Прогнозируемый запас в днях - показывает по артикулам товара количество заказов, среднее число заказов в день, запас в днях, остаток на складе и объём, необходимый для поставки товара на склад с датой прогноза на один месяц. Данные отсортированы по возрастанию запаса в днях и по убыванию числа заказов, что позволит отследить наиболее востребованные товары и вовремя поставить необходимое количество на склад. К таблице применимы фильтры по границе размера заказа и текущему остатку на складе.
 - Товары с наименьшим числом заказа - содержит список артикулов товаров, которые заказываются в наименьшем количестве и их объём на складе, данные можно ограничить по числу заказов за выбранный период.
 - Наличие товаров на складах - перечислены имеющиеся товары по складам и их текущий остаток.
 - Отсутствующие товары по складам - содержит список артикулов по складам, которых нет на складе.
 - История остатков - в таблице установлен фильтр для хранения данных об остатках на складах за последние 90 дней, полученные данные от заказчика содержат данные с 22 января 2023 года.

К графикам и таблицам установлены фильтры по дате заказа, складу, бренду, категории, товару и артикулу. Фильтр 'дата заказа' применим ко всем визуализациям, кроме графика 'Распределение товаров по складам на текущую дату', так как он содержит данные только на текущую дату. Историю остатков по складам можно увидеть в соответствующей таблице 'История остатков'.
 