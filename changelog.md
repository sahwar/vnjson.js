### changelog

= v0.8.5 =
> 2017.10.15
  * Внедрил модуль unfetch для нативного использования ajax
  * Дабавил вызов функции parse() в метод setLabel

= v0.8.4 =
> 2017.06.29
  * Сделал добавление [assets] в объект [game], тем самым реализовав пулл всех ресурсов.

= v0.8.3 =
> 2017.06.27
  * Убрал выполнение функции parse() из метода setLabel()
    т.к. ломается ход выполнения скрипта

= v0.8.2 =
> 2017.06.26
  * Убрал из стандартного api конструктор Events
  * Убрал объект plugin, теперь его функции выполняет fn 
  * Переименовал событие setlayers на setscreens в плагине vnjson-get-screens

= v0.8.1 =
> 2017.06.10
  * Расширил стандарное api конструктором Events

= v0.8.0 - harmony =
> 2017.06.06 
  * Заменил событие 'init' на 'getscreens'
  * Убрал параметры для методов prev/next
  * Переработал метод prev. Что бы он мог прыгать и открывать старые экраны. Но пока не получается делать это корректно.
  * Добавил logo
  * Расширил параметр game параметрами pacakge, settings.

= v0.7.9 =
> 2017.06.01
  * Метод parse() теперь возвращает vnjs
  * Исправил плагин vnjson-screen. Теперь сокрытие экранов происходит корректно
  * Добавил подключение модулей через метод [ .fn ]
  * Добавил в объект контекста ctx.data //userData
  * Параметр конфигурации screenPrefix заменен на prefix

= v0.7.8 =
> 2017.05.22
  * Вместо модуля getScene, теперь будет событие getscene, которое генерирует модуль vnjson-jump
  * Переименовал ветод ctx.label в ctx.labelName
  * В качестве параметра .parse('jump: /scene/entry') теперь можно указать строку.
  * Поправил аргумет строку метода parse. Теперь можно указывать параметр как с пробелом так и без.
  * Написал плагин vnjson-screen. Для показа экранов


= v0.7.7 =
> 2017.05.14
  * Начал писать тесты для библиотеки vnjs.
  * Добавил возможность вносить параметр размер шага в в навигацию prev next.
  * Написал функцию setCharacters(characters)
  * vnjs.off - removeEventListener
  * Довел до ума переходы(jump'ы) по меткам и сценам.
  * Переделал обработчик персонажей. Теперь персонажи
    объявляются как события. Вне сцены.
  * Удалил метот util, а его метот slitPathName перенес в плагин vnjson-jump

= v0.7.5 =
> 2017.04.30
  * Пересобрал vendor. Теперь из жизненно необходимых зависимостей осталось только minivents.js. Все остальное вынесоно в зависимости подключаемых внешне модулей vnjs.simpleModule = ()=>{console.log('simple-module')}
  * Всё лишнее убрал в сборшик проектов vnjson-cli
  * Вынес объявление параметров сцены в функцию setScene(nameScene, sceneObject);
  * setLabel(labelName, labelArray);

= v0.7.3  =
> 2017.04.28
  * Добавил плагин pathname
  * Внедрил во внутреннее API событие (parse) 
  * Сделал систему экранов.(screen) - Одноименное событие
    подгружающие кусок html и вещает событие с именем аргумента.
  * Вынес событие init в отдельный плагин
  * Сделал main-menu. А так же плагин обрабатывающий этот экран
  * Стандартное разрешение игры теперь 800x480px. Отказ от квадратного экрана в пользу прямоугольника. 

= v0.7.1 =
> 27.04.2017
  * Внедрил событийность. 
  * Вынес событие (jump) в плагин.
  * Расширил нативное api методами ['preload', 'loaded', 'next', 'prev', 'autorun']
  * Довел до ума систему автозапуска плагинов.
  * Переписал навигацию внутри label'ов, оставил место для перемотки назад. 
  * Изменил спецификацию сцены. Параметр characters раньше был массиво, теперь объект.

= v0.5.7 =
> 22.04.2017
  * Упорядочил систему плагинов. 
  * Построил базавую структуру механизма сохранения и загрузки ВН
  * В событии (alias) набросал возможность посимвольного вывода текста. Правда работает каряво, потому пока закомментирую.

= v0.4.9 =  
> 13.03.2017
  * Набросал спецификацию сцены
  * Начал переписывать все занаво
