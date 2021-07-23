# WebTest

--------

# Замечания

## картинки
- различие картинок (контентные(смысловые) и декоративные) 
    - есть два типа картинок на сайте: 
        - смысловые - несут какую либо информацию, которая важна на сайте (проверить так ли это довольно просто, закрываешь рукой картинку и если смысл сайта потерялся или пропала какая то важная информация то это контентная картинка)
        - декоративные - картинки для общей состовляющей всего сайта, несут чисто декоративный характер (при желании их можно можно убрать из общего контекста и смысл сайта не исчезет) `дополнение:` для различия в коде их можно давать через background-image какому либо диву

- название:
    - можешь для удобства папку с картинками назвать по другому - `img`, `images`, для более нормально понимая что там находится
    - посмотри на название картинок, они должны быть в едином стиле: называешь картинки с большой буквы, то все картинки тоже должны начинаться с большой буквы и тд

- ошибки: 
    - не подгружаются картинки так как названы по другому (смотри пример в html на 45 - 49 строках)

- alt в картинках:
    - альт дается в том случае если картинка несет какую либо смысловую нагрузку в сайте, в ином случае оставляй альт пустым

## отступы в коде

- html:
    - сделай отспупы везде одинаковыми, чтобы не было такого что некоторые теги расположены ближе другие глубже - все по `иерархии` тегов, можешь использовать для этого расширения - Prettier в VS Code его несложно найти

- css 
    - сильных замечаний в css нет, единственное - `адекватное название классов`, они должны коротко сообщать для чего они используются, чтобы по названию класса было понятно к чему относится блок, класс должен описывать содержимое контента, которые в нем находится
    
    - технологии названия классов: 
        - используй `BEM в именовании классов` ([BEM]"https://ru.bem.info/methodology/css/")
        - коротко о главном: даешь блоку навигации класс "navigation", всем его детям даешь логическое название - navigation__logo, navigation__links и тд (почитай про БЕМ)

    - `переменные и компонентный подход`
        - используй переменные для кода - для цветов, общих параметров (например кол-во пикселей для border-radius) это ты определяешь по макету, названия переменных должны быть абстрактными для понимая к чему она относится, чтобы если захочешь можно было быстро поменять цвет в переменной и он заменится у блока
            - так же в переменные можно засунуть шрифт который ты будешь использовать, через @font-family - `погугли`

        - `компоненты` - для удобства раскидай все по разным css файлам, переменный в файл root/variables.css, и для каждого блока в html свой файл css, header/footer.css, а на странице будет подключен только `один` файл css - style.css там сделаешь все импорты других файлов стилей 
