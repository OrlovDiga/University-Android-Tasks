# Лабораторная работа №1. Layouts


## Цели
* Ознакомиться со средой разработки Android Studio
* Изучить основные принципы верстки layout с использованием View и ViewGroup
* Изучить основные возможности и свойства LinearLayout
* Изучить основные возможности и свойства ConstraintLayout

## Задачи и решения
### Задача 1.  LinearLayout
#### Задание
Создайте layout ресурсы для следующих макетов экрана с использованием [LinearLayout](https://developer.android.com/guide/topics/ui/layout/linear).

Изображение 1 согласно [варианту](https://github.com/OrlovDiga/android-lectures/blob/master/labs/01/linear/14.png).

Изображение 2 согласно [варианту](https://github.com/OrlovDiga/android-lectures/blob/master/labs/01/linear/01.png).

#### Указания
* Изучите LinearLayout по документации от производителя ОС: https://developer.android.com/guide/topics/ui/layout/linear. Опишите свои наблюдения в отчете.
* Обратите внимание на атрибуты layout_weight, gravity, layout_gravity, orientation, layout_height, layout_width. Опишите их поведение и использование при решении задач в отчете (прим.: могут для решения задач могут потребоваться на все атрибуты).
* Изучите получившийся XML код. Докажите, что он не содержит избыточных тегов и атрибутов (например, продемонстрируйте, что удаление любого из тегов/атрибутов приведет к другой верстке)
* Многие задачи можно решить разными способами. Предложите два решения хотя бы для одной из задач.

### Решение

Изучили LinearLayout в документации от производителя. Из это вывели, что основная суть LinearLayout это представление его дочерних элементов в одном направлении - либо горизонтально, либо вертикально. Также познакомились с некоторыми его опциями, например такими, как:
**_layout_weight_** - это некоторый вес объекта, в соответствии с которым этот объект будет занимать доступное ему пространство; __*gravity*__ - задает позиционирование содержимого внутри объекта; __*layout_gravity*__ - задает позиционирование объекта относительно его родителя; __*orientation*__ - задает некоторое направление, в котором будут компановаться объекты; __*layout_height*__ - обозначает высоту объекта; __*layout_width*__ - обозначает ширину объекта.

Для отображения объектов в нужном нам виде воспользуемся LinearLayout c горизонтальным или вертикальным отображением. Так же нам понадобятся такие теги для объектов, как *android:layout_weight="1"*, при этом задав *android:layout_width="0dp"* или *android:layout_height="0dp"*. Также для одного из вариантов нам потребуется сделать отступ между объектами. Для этого воспользуемся тегом *android:layout_marginBottom="150dp"*

Вот сами xml разметкки для данной задачи в соответствии с вариантом:
* [Первая разметка](https://github.com/OrlovDiga/University-Android-Tasks/blob/master/app/src/main/res/layout/lab_1th_task_1th_var_14th.xml)
* [Вторая разметка](https://github.com/OrlovDiga/University-Android-Tasks/blob/master/app/src/main/res/layout/lab_1th_task_1th_var_1th.xml)

Мы убрали все возможные теги и для проверки этого, давайте попробуем удалить один из них. Например, при удаление _android:layout_height="0dp"_ из любого виджета у нас возникает ошибка 'layout_height' attribute should be defined'.

Так же давайте решим одну из наших задач вторым способом - с помощью установки конкретных dp значений, для всех трех заданных объектов.
[Соответсвующая разметка](https://github.com/OrlovDiga/University-Android-Tasks/blob/master/app/src/main/res/layout/lab_1th_task_1th_var_1th_version_2.xml)

### Задача 2. ConstraintLayout
#### Задание
Решите задачу 1 (обе подзадачи) с использованием [ConstraintLayout](https://developer.android.com/training/constraint-layout)

#### Указания:
* Изучите ConstraintLayout по документации от производителя ОС: https://developer.android.com/training/constraint-layout. Опишите свои наблюдения в отчете.
* Обратите внимание на атрибут layout_constraintDimensionRatio, layout_constraintHorizontal_weight, layout_constraintVertical_weight (прим.: может не использоваться для решения задач).
* Изучите получившийся XML код. Докажите, что он не содержит избыточных тегов и атрибутов

### Решение

Для решения данной задачи воспользуемся constraint_layout. Основные теги, которые должны придать нам нужную разметку: *app:layout_constraintHorizontal_weight="1"*, и в одном случае *android:layout_marginBottom="150dp"*. Остальное будет мало чем отличаться от предыдущего задания.

Вот сами xml разметкки для данной задачи в соответствии с вариантом:
* [Первая разметка](https://github.com/OrlovDiga/University-Android-Tasks/blob/master/app/src/main/res/layout/lab_1th_task_2th_var_14_th.xml)
* [Вторая разметка](https://github.com/OrlovDiga/University-Android-Tasks/blob/master/app/src/main/res/layout/lab_1th_task_2th_var_1th.xml)

### Задача 3. ConstraintLayout
Создайте layout ресурс для следующего макета экрана с использованием ConstraintLayout.

Изображение 3 согласно [варианту](https://github.com/OrlovDiga/android-lectures/blob/master/labs/01/constraint/lab01_constraint_v14.png).

### Решение

Для решения данной задачи будем использовать зададим квадратный ConstraintLayour в центре экрана. Для удобной компановки объктов в нем будем использовать chains, и просто задавать соответствующие размеры dp.

[Клик, и разметка откройся!](https://github.com/OrlovDiga/University-Android-Tasks/blob/master/app/src/main/res/layout/lab_1th_task_3th_var_14_th.xml)

## Заключение
Мы ознакомились со средой разработки Android Studio, изучили осовные принципы верстки layout с использованием View и ViewGroup, изучили основные возможности и свойства LinearLayout и ConstraintLayout.
