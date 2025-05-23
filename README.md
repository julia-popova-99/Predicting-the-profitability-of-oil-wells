# Выбор прибыльной локации для нефтяной скважины
Компании «ГлавРосГосНефть» нужно решить, где бурить новую скважину.  Предоставлены пробы нефти в трёх регионах: в каждом 100 000 месторождений, где измерили качество нефти и объём её запасов. Постройте модель машинного обучения, которая поможет определить регион, где добыча принесёт наибольшую прибыль.
**Цель исследования:** определить, где бурить новую скважину.
    
**Задачи исследования:**
1) Построить модель для определения региона, где добыча принесёт наибольшую прибыль;

2) Проанализировать возможную прибыль и риски техникой Bootstrap.

**Описание данных**

>Данные геологоразведки трёх регионов находятся в файлах: 
+ [/datasets/geo_data_0.csv.](https://code.s3.yandex.net/datasets/geo_data_0.csv)
+ [/datasets/geo_data_1.csv.](https://code.s3.yandex.net/datasets/geo_data_1.csv)
+ [/datasets/geo_data_2.csv.](https://code.s3.yandex.net/datasets/geo_data_2.csv)

Где:
+ `id` — уникальный идентификатор скважины;
+ `f0, f1, f2` — три признака точек (неважно, что они означают, но сами признаки значимы);
+ `product` — объём запасов в скважине (тыс. баррелей).

Шаги для выбора локации:

+ В избранном регионе ищут месторождения, для каждого определяют значения признаков;
+ Строят модель и оценивают объём запасов;
+ Выбирают месторождения с самым высокими оценками значений. Количество месторождений зависит от бюджета компании и стоимости разработки одной скважины;
+ Прибыль равна суммарной прибыли отобранных месторождений.

**Ход исследования:**
1. Загрузка и подготовка данных
2. Обучение и проверка модели для каждого региона
3. Подготовка к расчёту прибыли
4. Расчёт прибыли и рисков для каждого региона
5. Вывод по исследованию
