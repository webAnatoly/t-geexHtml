## Starter kit for building pages with html/scss
Базовый набор для начала верстки с препроцессором sass, postCSS, cssnano и livereload. 


### INSTALL
Почему-то **npm install** из packag.json падает на установке gulp-sass (permission denied), но если отдельно запустить **npm install gulp-sass --save-dev** то все норм.

Второй вариант установки с флагом --unsafe-perm

**npm install --unsafe-perm**

После успешной установки запустить **gulp dev** и можно творить :)


### SAAS 7 TO 1 PATTERN  
    scss  
      abstracts  
        _functions.scss  
        _mixins.scss  
        _variables.scss  
      base  
        _normalize.scss  
        _animations.scss  
        _base.scss       # базовые стили для всего документа  
        _typography.scss # всё что касается шрифтов  
        _utilities.scss  # вспомогательные классы  
      components  
        _button.scss  
        _dropdown.scss  
        ...              # Etc.  
      layout  
        _grid.scss  
        _header.scss  
        _footer.scss  
        _navigation.scss  
        _sidebar.scss  
      pages  
        _home.scss  
      themes  
        _theme.scss  
      vendors  
        _bootstrap.scss   # Bootstrap  
        ...               # Etc.  
    main.scss  

**abstracts** - в этой папке лежат абстрактные сущности, такие как переменные, миксины, функции

**base** - базовые стили, анимация, шрифты, вспомогательные классы

**components** - отдельные, независимые блоки по БЭМ, например кнопки, модульные окна, и прочие самостоятельные смысловые фрагменты.

**layout** - все что касается организации отображения контента на всем сайте, на всех страницах. Например header, сайдбар, навбар, сетки. Ну конечно граница между layout и components весьма условна. 

**pages** - страницы сайта. Если это лендинг, то тут будет один файл _home.scss

**themes** - для тем, если они есть

**vendors** - для сторонних стилей

