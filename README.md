# adaptive-layout
https://llstudent83.github.io/adaptive-layout/

В рамках дипломного проекта вам необходимо сверстать макет сайта для трех групп устройств: десктопные экраны, планшеты и смартфоны.

1. 1200px и более,
2. 768px - 1200px,
3. 360px - 768px,

Макеты сайта для различных экранов выглядят так:

![Layout](./img/layouts.jpg)

### Кроссбраузерная верстка
В рамках проекта сверстанные макеты должны корректно отображаться на следующих типах устройств:
- компьютер с операционной системой Windows и Mac OS,
- планшеты и смартфоны с операционной системой iOS,
- планшеты и смартфоны с операционной системой Android.

Кроме поддержки основных типов устройств также требуется, чтобы верстка корректно работала в следующих браузерах:
- Последняя версия Google Chrome,
- Последняя версия Mozilla FireFox,
- Последняя версия Edge,
- Последняя версия Opera,
- Последняя версия Safari,
- Последняя версия Mobile Safari,
- Последняя версия Mobile Chrome.

В случае, если у вас нет какого-то устройства, следует его найти. Тестирование на реальных устройствах является обязательным навыком современного специалиста.

### Семантическое использование тегов
В макетах проекта содержатся следующие элементы:
- Разделы,
- Заголовки,
- Ссылки,
- Изображения,
- Подписи,
- Абзацы.

Все эти элементы имеют специальные теги в стандарте HTML5, поэтому в рамках проекта вам необходимо их использовать.

К примеру, следующий код является грубой ошибкой:
```html
<div class="header">
  <div class="title">Заголовок сайта</div>
</div>
```

Кроме использования семантических тегов, также нужно правильно вкладывать теги по типу контекста. Запрещается в строчный элемент помещать блочный. Например, следующий код будет ошибочным:

```html
<span class="information">
  <h2 class="title">Заголовок блока</h2>
</span>
```

### Семантические названия атрибутов
Кроме использования семантических тегов также необходимо давать семантические названия значениям атрибутов. Запрещается использовать транслит. 

Пример:
```html
<header class="shapka"></header>
```
Данный пример является грубой ошибкой. Название класса `shapka` следует заменить на `header`. Пример корректного названия:
```html
<header class="header"></header>
```
### Валидная верстка
После полной реализации верстки необходимо ее протестировать с помощью сервиса [W3C Markup Validation Service](https://validator.w3.org). В итоговом отчете не должно быть ошибок или предупреждений.

### Соответствие верстки макету
Итоговый проект должен быть копией макетов, предоставленных дизайнером. При реализации допускаются следующие отличия:
- толщина шрифта в браузерах и фотошопе,
- межсимвольное расстояние,
- различия в отступах — до 2px.

### Реализация сетки
Реализовать сетку страницы вам нужно при помощи `flexbox`. Запрещено использовать библиотеки, которые уже имеют готовые классы для сетки (например, Twitter Bootstrap, Zurb Foundation и другие).

Также запрещено использовать следующие способы решения задачи:
- таблицы,
- float-сетка,
- сетка с помощью `inline-block` элементов,
- CSS Grids.

### Промежуточные состояния между макетами
Дизайнер подготовил три макета отображения страницы для устройств с шириной экрана 320px, 768px и 1920px. Но дизайнер не предоставил отображения страницы в промежуточных состояниях, поэтому их нужно реализовать с помощью принципа «Резиновая верстка».

Таким образом, на экранах с шириной больше 1920px фоновые блоки будут растягиваться на всю ширину экрана, а их контент будет центрироваться.

На устройствах с шириной экрана, попадающей в диапазон от 961px до 1920px, вам нужно реализовать дизайн макета `surface_desktop.psd`.

Для устройств с шириной экрана, попадающей в диапазон от 641px до 960px, вам нужно реализовать резиновый дизайн макета `surface_768.psd`.

Для устройств с шириной экрана, попадающей в диапазон от 640px и меньше, вам нужно реализовать резиновый дизайн макета `surface_320.psd`.

Для верстки изображений в промежуточных состояниях разрешается использовать изображения из макетов, более подходящие для данной ширины экрана. Например, блок «Be active» в макете `surface_desktop.psd` имеет ширину 960px, а в макете `surface_768.psd` — 768px. Соответственно, для экрана с шириной 960px больше подойдет версия из макета `surface_desktop.psd`.

### Добавление меньшего или большего количества контента в блоки
Вам обязательно нужно протестировать блоки с информацией, добавив в них больше или меньше контента, чем представлено в макетах. Блоки не должны сломать соседние блоки, текст при этом должен быть полностью читаемым.

### Ошибки загрузки изображений
При верстке изображений вам нужно предусмотреть ситуацию, когда по какой-либо причине они не загрузятся.

- В случае контентных изображений верстка не должна сломаться, а вместо изображения должен отображаться альтернативный текст, из которого станет понятно, что было изображено на картинке.

- Для декоративных изображений вам необходимо подобрать подложки для текста, чтобы текст был читаемым в любой ситуации. 

### Запрещается использовать CSS методологии
В рамках курса мы не рассматривает CSS методологии такие как: БЭМ, OOCSS, SMACSS и другие. Поэтому в дипломе запрещается их использовать.

### Запрещается использовать готовые библиотеки
В рамках дипломного проекта запрещается использовать готовые библиотеки (например, normalize.css, reset.css, bootstrap и другие). Весь код вы должны написать самостоятельно.

### Запрещается использовать CSS препроцессоры или PostCSS
В рамках курса мы не рассматриваем способы организации кода с использованием CSS препроцессоров и PostCSS. Поэтому в дипломе вам запрещается их использовать.

### Запрещается использовать autoprefixer
Для реализации кроссбраузерной верстки дипломного проекта вам не потребуется autoprefixer, поэтому его использование запрещено.