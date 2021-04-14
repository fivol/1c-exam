# Задача для отборочного испытания на кафедру КИС (1С)

## Код задачи: 143

## Условие задачи "Крестики-нолики"


На вход программе подаётся изображение игрового поля в крестики-нолики.

Необходимо обработать его и провести "победную" линию (перечёркивающую три одинаковых символа по правилам игры). Игровое поле может не содержать победителя (Тогда никакую линию проводить не надо). Гарантируется, что существует только одна победная линия. 

Формат изображения -- png. Игровое поле находится в произвольном месте изображения, однако гарантируется, что все символы имеют одинаковый размер/толщину и центрированы относительно секторов. Линии игрового поля проведены параллельно краям изображения. Если алгоритм решения будет требовать определённого размера/толщины фигур -- отразите это в документации.



## Решение
Всё решение находится в файле `1c-exam.ipnb`
HTML версия в случае ошибок отображения `1c-exam.html`

Для чтения изображения использова библиотека `imageio`
https://pypi.org/project/imageio/

### Основные этапы
1. Считать картинку из файла в формате `png`
2. Локализовать доску, найти направляющие
3. Найти области каждой фигуры и определить, какого она типа:
    - Крестик
    - Нолик
    - Пустота
4. В полученном массиве 3 x 3 найти 3 повторяющиеся фигуры по вертикале,
горизонтали или диагонали
3. Определить координаты начала и конца линии
4. Нарисовать линию на изображении
5. Сохранить картинку

## Примеры
В репозитории лежит 2 примера
- `example1.png` -> `example1_result.png`
- `example2.png` -> `example2_result.png`


## Необходимо реализовать (TODO)
*Действия по усовершенствованию функционала*
1. Заменить подсчёты суммы на `np.sum`, это повысит скорость в разы
2. Перенести в `.py`, разбить на несколько файлов и классов
3. Сделать консольный ввод-вывод с помощью `argparse`
4. Протестировать программу на большом количестве изображений. 
Я бы использовал `pytest`

## Автор
Новичков Борис, МФТИ ФПМИ
