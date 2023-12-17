# Проект "Посмотри в окно"
***
## Структура сайта
Семантически сайт поделен на несколько блоков и секций:
__Блок main__ - Основное содержимое страницы, который, в свою очередь, состоит из нескольких секций:
  * __Секция result__  - секция сайта, в котором прогружается видео, подходящее по критериям, указанным в поиске;
  * __Секция content-details__ - секция сайта, в котором отображаются все варианты, подходящие по критериям поиска;

***
## Функционал проекта
### 1. Организация файлов в проекте
Проект создан по методологии БЭМ, аайловая структура в реализована по схеме Nested:
* Каталог styles - содержит блоки проекта, модификаторы и элементы;
* Каталог scripts - содержит JS скрипты, используемые в проекте;
* Каталог pages - содержит файл Index.css, в котором указанны ссылки на все CSS стили проекта;
* Каталог vendor - содержит сторонние CSS файлы.

### 2. Используемые технологии
Все элементы страницы хранятся в родительском блоке `body`.
В проекте используется файл `styles.css`, в указываются глобальные стили, такие как обнуление стандартных отступов элементов, указание ширины страницы и тд.

В проекте используются  шрифты `Fira Sans Condensed` и `Oswald`.

В проекте реализован прелоадер - пока загружаются данные, пользователь видит анимацию процесса загрузки.

Принцип работы скрипта:

1. При загрузке страницы скрипт получает данные из внешнего источника, отрисовывает пять карточек с видео и кнопку, чтобы подгрузить дополнительные карточки. Ещё он подставляет адрес первого из загруженных роликов в тег <video> внутри крупного блока на странице.
2. Скрипт отслеживает клик по карточкам и переключает текущее видео в зависимости от выбранной карточки.
3. Cкрипт следит за отправкой формы. После отправки он ищет в базе данных совпадения по введённым параметрам и перерисовывает страницу с данными, полученными из нового запроса.
4. В случае ошибок на место блока с видео подставляется блок с сообщением об ошибке. Пока идёт поиск, в блоки с видео и карточками подставляются прелоадеры, отображающие анимацию процесса загрузки.

Шаблоны:
1. Шаблон пункта списка с карточкой видео — в него мы подставляем данные и создаём столько карточек на странице, сколько нужно, добавляя их в список.
2. Шаблон прелоадера — пока данные загружаются, мы создаём экземпляры прелоадера и вставляем в зоны, куда будет вставлен контент. Когда контент готов, мы убираем прелоадеры.
3. Шаблон кнопки «Показать ещё» — мы подставляем эту кнопку в конец списка карточек каждый раз, когда доступны дополнительные видео. Нажатие на эту кнопку подгружает пять дополнительных карточек.
4. Шаблон блока с ошибкой — в зависимости от типа ошибки, мы выбираем текст для неё, создаём экземпляр шаблона с текстом и вставляем на страницу.

### 3. Планы по доработке
1. Реализовать адаптивное масштабирование в диапазоне от 320px

### 4. Ссылка на репозиторий GitHub
[Посмотри в окно](https://github.com/sergey-pyschkin/posmotri_v_okno)

# posmotri_v_okno

