Задача
Необходимо реализовать игру "Шахматы" с возможностью:

Играть двум игрокам с одного компьютера
Играть двум игрокам по сети через сервер
Играть на одном компьютере против ИИ противника (Hacker Score)
UX прототип
Базовый макет с прототипом функциональности

Возможно вносить любые изменения в изначальный дизайн, однако все элементы из прототипа, кроме аватара, должны присутствовать, в любом виде.

Требования к функционалу приложения
Приложение должно быть написано на Typescript
Все фигуры поворачиваются к игроку, имеющему право хода. Не должно быть фигур, которые смотрят в разные стороны.
До запуска игры должна быть возможность изменить имя игрока.
До запуска игры должна быть возможность выбрать режим (по сети\в режиме игры двух игроков с двух пк\в режиме игры с ботом (не обязательно)).
По клику на кнопку "Старт" должен запуститься игровой цикл.
Каждая фигура должна ходить согласно общепринятым правилам шахмат.
У каждого игрока должна отображаться история ходов, в которой должны быть отражены:
Фигуры, которыми были совершены ходы
Время совершения ходов
Начальные и конечные клетки совершения хода фигур в формате: E2-E4
Должен быть реализован таймер игры, ведущий отсчет от начала игры.
После совершения хода Время таймера должно совпадать со временем указанным в истории ходов.
Для любого игрока должна быть возможность принять поражение. В случае принятия поражения победа засчитывается оппоненту.
Во время хода игрок, который совершает ход, должен быть помечен соответствующей иконкой.
Должна быть реализована механика рокировки.
В случае ситуации "Шах", должна быть подсветка ячеек ходов из-за которых такая ситуация возникла.
В случае ситуации "Шах", ячейка на которой находится король должна быть выделена.
В случае ситуации "Мат", должна быть подсветка ячеек ходов из-за которых такая ситуация возникла. Цвет должен быть отличен от цвета использованного в событии "Шах".
В случае ситуации "Мат", ячейка на которой находится король должна быть выделена.
В случае ситуации "Мат", игрок, фигура которого поставила "Мат" объявляется победителем.
Победитель должен быть выделен соответствующим образом.
После выигрыша\поражения игрока таймер должен остановится.
После завершения игры игроку должен быть предоставлен следующий выбор:
Вернуться в лобби, где игрок сможет начать новую игру.
Просмотреть повтор текущего матча. (В случае если реализован механизм просмотра "Записи" матчей.)
Фигуры должны передвигаться по доске с помощью drag-and-drop.
Доступные ходы фигуры должны быть подсвечены.
Ход должен завершаться после того как фигура была поставлена на новую ячейку.
Первый ход должна совершать "Белая" сторона.
Задания повышенной сложности:
Реализовать механику ситуации "Ничья" по следующим ситуациям:
Соглашение сторон
Пат (сторона, имеющая право хода, не может им воспользоваться)
Реализовать ИИ бота противника.
Особенности реализации в зависимости от выбранного типа игры:
Режим игры двух игроков с одного ПК:

При передаче хода другому игроку должна быть реализована следующая анимация:
Поле а1 должно быть чёрного цвета.
Символы, отвечающие за маркировку сетки таблицы должны исчезнуть (Если они предусмотрены выбранным дизайном) (A-H, 1-8).
Доска должна развернуться на 180 градусов.
Символы, отвечающие за маркировку сетки таблицы должны появиться (Если они предусмотрены выбранным дизайном) (A-H, 1-8).
eslint
eslint должен быть настроен

eslint включен в package.json,
вы должны использовать конфигурацию eslint-config-airbnb-base
весь код должен быть проверен
проверка eslint выполняется запуском команды npm run lint
Ограничения
задание должно работать в Chrome
Использование material design, semantic-ui или bootstrap допускается
Разрешается Angular / React / Vue / Svelte с разрешения ментора
Вы можете использовать препроцессоры
Вы можете общаться, переписываться в чате, гуглить и использовать stackoverflow
Вы можете использовать lodash.js
Последовательность выполнения
создать папку codejam-chess. Все файлы проекта должны находиться в папке "codejam-chess". Организация кода внутри папки на ваше усмотрение.
Создайте HTML-файл с основным макетом и CSS-стилями для него. Тег body в html документе должен оставаться пустым.
Реализовать страницу Лобби с возможностью запуска игры и смены имени игрока
Базово реализовать страницу игры (Игровое поле, фигуры, иконки соперников, таблицы ходов)
Реализовать drag and drop передвижение фигур
Реализовать перемещение фигуры кликом по ней мышкой, затем по клетке назначения
Добавить ограничения хода для разных фигур
Реализовать механику "Рокировка", учитывая то, что рокировка невозможна в ситуациях:
между королём и ладьёй присутствуют фигуры
король находится под шахом
король проходит через атакованное поле
король в результате рокировки становится на атакованное поле
король сделал хотя бы один ход с начала партии
ладья, которая задействована в рокировке, сделала хотя бы один ход с начала партии
Реализовать механику взятия фигуры противника.
Реализовать механику "Шах"
Реализовать механику "Мат"
Реализовать механику Прекращения текущей игры (Выход в лобби с присвоением поражения игроку совершавшему ход).
Добавить таблицы ходов для каждого из игроков.
Реализовать таймер текущей партии, который начинается со старта партии и завершается после победы\поражения одного из игроков.
Реализовать анимацию поворота доски при смене хода.
При желании приступить к выполнению задания повышенной сложности.

