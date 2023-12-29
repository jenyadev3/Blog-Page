# blog-page
Дипломный проект в рамках курса Нетологии «Адаптивная и мобильная верстка»

В рамках дипломного проекта необходимо было сверстать макет сайта для трёх групп устройств: десктопные экраны, планшеты и смартфоны.

Макеты сайта для различных экранов выглядят так:

![Layout]( https://github.com/netology-code/mq-diploma/blob/master/img/layouts.jpg)

- `NOEMI_mq_desktop.psd` — макет для экрана шириной `1200px` и более;
- `NOEMI_mq_tablet.psd` — макет для экрана шириной `768px`;
- `NOEMI_mq_mobile.psd` — макет для экрана шириной `360px`.

## Требования
### Кроссбраузерная вёрстка
В рамках проекта свёрстанные макеты должны корректно отображаться на следующих типах устройств:
- компьютерах с операционными системами Windows и macOS,
- планшетах и смартфонах с операционной системой iOS,
- планшетах и смартфонах с операционной системой Android.

Кроме поддержки основных типов устройств требуется, чтобы вёрстка корректно работала в следующих браузерах:
- Последняя версия Google Chrome,
- Последняя версия Mozilla Firefox,
- Последняя версия Edge,
- Последняя версия Opera,
- Последняя версия Safari,
- Последняя версия Mobile Safari,
- Последняя версия Mobile Chrome.

### Соответствие вёрстки макету
Итоговый проект должен быть копией макетов, предоставленных дизайнером. При реализации допускаются небольшие отличия:
- толщина шрифта в браузерах и фотошопе,
- межсимвольное расстояние,
- различия в отступах до `5px`.

### Промежуточные состояния между макетами
Дизайнер подготовил 3 макета отображения страницы для устройств с шириной экрана `360px`, `768px` и `1200px`. Но дизайнер не предоставил отображения страницы в промежуточных состояниях, поэтому их нужно реализовать с помощью принципа «Резиновая вёрстка».
Таким образом, на экранах с шириной больше `1200px` фоновые блоки будут растягиваться на всю ширину экрана, а их контент будет центрироваться.
На устройствах с шириной экрана от `1200px` и более нужно реализовать дизайн макета `NOEMI_mq_desktop.psd`.
Для устройств с шириной экрана, попадающей в диапазон от `641px` до `1200px`, нужно реализовать резиновый дизайн макета `NOEMI_mq_tablet.psd`.
Для устройств с шириной экрана от `640px` и меньше нужно реализовать резиновый дизайн макета `NOEMI_mq_mobile.psd`.

### Состояния при повороте экрана
Вёрстка раздела «Сейчас в тренде» должна отличаться при портретной (вертикальной) ориентации экрана и при пейзажной (горизонтальной).
Для устройств с шириной экрана, попадающей в диапазон от `641px` до `1200px`, при портретной ориентации экрана карточки трендов должны быть выстроены в 2 колонки, а при пейзажной ориентации — в 4.
Для устройств с шириной экрана от `640px` и меньше при портретной ориентации экрана должна быть 1 колонка с карточками, а при пейзажной — 2.

![Layout]( https://github.com/netology-code/mq-diploma/blob/master/img/rotation.jpg)

### Вёрстка всплывающей формы (pop-up)
Каждый макет содержит всплывающую форму на слое `Pop-up`, этот слой по умолчанию скрыт. Свёрстанная форма должна отображаться по центру экрана — поверх вуали, затемняющей страницу. Не нужно реализовывать всплытие формы и её скрывание при клике на крестик. Достаточно, чтобы форма была в разметке.

![Layout]( https://github.com/netology-code/mq-diploma/raw/master/sources/NOEMI_mq_desktop_popup.jpg)

### Вёрстка бургер-меню
Не нужно реализовывать сворачивание и разворачивание бургер-меню при клике на иконку. В зависимости от макета должна быть видима либо иконка, либо меню.

### Семантическое использование тегов
В макетах проекта содержатся следующие элементы:
- разделы,
- заголовки,
- ссылки,
- изображения,
- подписи,
- абзацы.

Все эти элементы имеют специальные теги в стандарте HTML5, поэтому в рамках проекта необходимо их использовать.
Кроме использования семантических тегов нужно правильно вкладывать теги по типу контекста. Запрещается в строчный элемент помещать блочный.

### Семантические названия атрибутов
Кроме использования семантических тегов необходимо давать семантические названия на английском языке в качестве значений атрибутов. Не использовать транслит. 

### Валидная вёрстка
После полной реализации вёрстки протестировать её с помощью сервиса [W3C Markup Validation Service](https://validator.w3.org). В итоговом отчете не должно быть ошибок или предупреждений.

### Реализация сетки
Реализовать сетку страницы нужно при помощи `flexbox`. Использование библиотек, которые уже имеют готовые классы для сетки (Twitter Bootstrap, Zurb Foundation и другие), будет считаться ошибкой.
Также ошибкой будет считаться использование следующих способов вёрстки сетки:
- таблицы,
- float-сетка,
- сетка с помощью `inline-block`-элементов,
- CSS Grids.

### Добавление меньшего или большего количества контента в блоки
Нужно протестировать блоки с информацией, добавив в них больше или меньше контента, чем представлено в макетах. Блоки не должны сломать соседние блоки, текст при этом должен быть полностью читаемым.

### Ошибки загрузки изображений
При вёрстке изображений нужно предусмотреть ситуацию, когда по какой-либо причине они не загрузятся.

- В случае контентных изображений вёрстка не должна сломаться, а вместо изображения должен отображаться альтернативный текст, из которого станет понятно, что было изображено на картинке.

- Для декоративных изображений необходимо подобрать подложки для текста, чтобы текст был читаемым в любой ситуации. 

### Не использовать CSS-методологии
В рамках курса не рассматриваются CSS-методологии — БЭМ, OOCSS, SMACSS и другие. Поэтому при работе над дипломом не использовать их.

### Не использовать готовые библиотеки
В рамках дипломного проекта не следует использовать готовые библиотеки — normalize.css, reset.css, bootstrap и другие. Весь код надо написать самостоятельно.

### Не использовать CSS-препроцессоры или PostCSS
В рамках курса не рассматриваются способы организации кода с использованием CSS-препроцессоров и PostCSS. Поэтому в дипломе не следует их использовать.

### Не использовать autoprefixer
Для реализации кроссбраузерной вёрстки дипломного проекта не потребуется autoprefixer, поэтому его использование не приветствуется.
