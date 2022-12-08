###Тестирование возможности записаться на обучение профессии «Тестировщик ПО»
####1.#### Перечень автоматизируемых сценариев
####1.1 Тестирование пролистывания страницы вниз до формы записи
####1.2	Тестирование попадание на страницу с каталогом курсов через нажатие на кнопку «Каталог курсов» на главной странице
####1.3	Тестировать попадание на страницу с каталогом курсов через нажатие на иконку «НЕО для начинающих»
####1.4	Тестировать попадание на форму заполнение записи на странице Каталог курсов нажатием на кнопки «Программирование» - «Профессия Тестировщик»
####1.5	Тестирование попадание на форму заполнение записи на странице Каталог курсов через «Полный каталог»
#####1.6	Тестирование страницы с записью на консультацию (автоматическое заполнение полей формы и нажатие на кнопку отправить)
#####1.6.1	Заполнение полей валидными данными, нажатие на кнопку «Записаться»
#####1.6.2	Заполнение полей валидными данными, нажатие на кнопку «Получить консультацию»
#####1.6.3	Заполнение поля студент не валидными данными, нажатием на «Записаться»
#####1.6.4	Заполнение поля студент не валидными данными, нажатием на «Получить консультацию»
#####1.6.5	Заполнение поля телефон не валидными данными, нажатием на «Записаться»
#####1.6.6	Заполнение поля телефон не валидными данными, нажатием на «Получить консультацию»
#####1.6.7	Заполнение поля e-mail не валидными данными, нажатием на «Записаться»
#####1.6.8	Заполнение поля e-mail не валидными данными, нажатием на «Получить консультацию»
###2. Перечень используемых инструментов с обоснованием выбора.
- Java , т.к поддерживает такие библиотеки как JUnit Jupiter, и инструменты управления проектом как Gradle
- Gradle – который упрощает работу, за счет того что:  умеет самостоятельно скачивать и устанавливать нужные зависимости (и зависимости зависимостей), а также компилировать проект, запускать автотесты.
- JUnit 5 фреймворк для тестирования отдельных участков кода. Использование JUnit позволяет проверить код программы без значительных усилий и не занимает много времени.  JUnit 5 управляет выполнением каждого метода тестирования, поддерживает многие аннотации, позволяющие упростить код и сэкономить время. 
- Selenide -фреймворк для автоматизированного тестирования веб-приложений , он помогает быстро писать код и упрощает его. Selenide помогает писать сценарии которые будут проверять работу веб-приложения: поиск нужных элементов, проверка событий, взаимодействие с UI. 
###3. Перечень необходимых разрешений, данных и доступов
#####3.1 Валидные данные для каждого из полей на форме «Записи на консультацию»
#####3.2 Не валидные для каждого из полей на форме «Записи на консультацию»
#####3.3 Обязательные для заполнения поля на форме «Записи на консультацию»
#####3.4 Необходим доступ к базе данных куда попадают данные с формы «записи на консультацию» после нажатие на кнопки «Записаться», «Получить консультацию»
###4. Перечень и описание возможных рисков при автоматизации.
Не желательно автоматизировать главную страницу и страницу «каталог курсов» т.к – нет необходимости вводить данные (т.е. не теряем время на ввод данных), на этих страницах GUI – тестирование, т.е. при автоматизации есть возможность появления багов, которых автоматизация не увидит (кнопка, ссылка стоит на нужном месте, либо другой баг, связанный с вёрсткой страницы). Так же есть возможно, внешний вид  главной страницы будет часто и кардинально меняться и придётся полностью переписывать тесты.
Автоматизировать тестирование страницы с записью на консультацию (страница на которой поля:  «студент», «номер телефона», e-mail) дает следующие плюсы: 
-регрессионное тестирование будет проходить быстрее: 
- нет необходимости тратить время на ввод данных, т.е. мы автоматизируем рутинную работу
 -все последующие «регрессионные» тесты будут проходить при «одинаковых условиях»
###5. Перечень необходимых специалистов для автоматизации.
QA- engineer, специалист по работе с базой данных
###6. Интервальная оценка с учётом рисков в часах.
6-9 часов

