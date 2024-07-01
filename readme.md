# Template - Файловая система для вашего сайта

Шаблон построен на импортах, что позволяет писать стили отдельно для мобильной и десктопной версии сайта, а также корректно подключать темную/светлую тему.
Преимущество в том, что вам не нужно переписывать или отменять стили для мобильной версии сайта на десктопе и наоборот.

**CSS папки и файлы**
В каждом блоке есть файлы base.css, mobile.css и desktop.css.
Файл base.css - прописываются базовые(общие) стили для элементов.
Файл mobile.css - прописываются стили для мобильной версии сайта и его элементов.
Файл desktop.css - прописываются стили для десктопной версии сайта и его элементов.

**Цвета**
Цвета работают вполне понятно, есть главные и вторичные цвета, светлая и темная тема сайта.
Напримере разберем файл styles/colors/dark.css, где прописаны следующие строки:
--color-back-primary: var(--color-black); - строка обозначает главный цвет фона.
--color-back-secondary: var(--color-darker); - строка обозначает вторичный цвет фона.
--color-text-primary: var(--color-white); - строка обозначает главный цвет текста.
--color-text-secondary: var(--color-lighter); - строка обозначает вторичный цвет текста.

В файле colors/light.css есть подобный код, который описывает цвета для светлой темы сайта.

Если на вашем сайте нет разделения на разные темы, вы можете отключить переключение тем.
Потребуется удалить в файле index.html строки:
<link rel="stylesheet" href="styles/light.css" media="(prefers-color-scheme: light)">
<link rel="stylesheet" href="styles/dark.css" media="(prefers-color-scheme: dark)">

и удалить файлы:
styles/dark.css
styles/light.css
styles/colors/dark.css
styles/colors/light.css
