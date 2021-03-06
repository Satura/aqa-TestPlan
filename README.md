### **Объект тестирования:** возможность записи на обучение профессии "Тестировщик ПО"


Будет произведено модульное:

 - отображение и работа на страницах сайта необходимых элементов интерфейса (кнопки, фильтры, меню и поля)

и интеграционное:
 - работа ссылок
 - отправка формой валидных данных в базу, для последующей обработки

функциональное тестирование.
 

## Перечень автоматизируемых сценариев

0. Открыть в браузере страницу https://netology.ru/

1. Сценарии перехода на страницу профессии:

    1.1 *Сценарий "Каталог курсов"*. 
    
       Кликнуть по кнопке "Каталог курсов".   
       Навести мышь на ссылку "Программирование".
       Кликнуть в ссылку "Тестировщик ПО".

    1.2 *Сценарий "Нео"*. 
    
       Кликнуть по элементу "НЕО для начинающих". 
       Выбрать в фильтре направления "Программирование". 
       Кликнуть в ссылку "Тестировщик ПО".
    
    1.3 *Сценарий "Актуальные темы"*. 
    
       Кликнуть в элемент "Программирование" в блоке "Изучайте актуальные темы".  
       Кликнуть в ссылку "Тестировщик ПО".
    
    1.4 *Сценарий "Программирование"*. 
    
       Найти на странице (в конце) ссылку "Программирование" и перейти по ней. 
       Кликнуть в ссылку "Тестировщик ПО".
	   
	Результат выполнения сценариев: переход на страницу профессии https://netology.ru/programs/qa

2. Сценарии перехода к форме записи на странице профессии:

	Входные данные: в браузере открыта страница профессии https://netology.ru/programs/qa
  
    2.1 *Сценарий "Блок презентации"*.
    
       На странице профессии кликнуть по кнопке "Записаться" в первом блоке страницы.
  
    2.2 *Сценарий "Блок гарантии"*.
    
       На странице профессии кликнуть по кнопке "Записаться" в блоке "Гарантия возврата денег.
    
    2.3 *Сценарий "Форма записи"*.
    
       Найти форму записи в конце страницы. 
	
	Результат выполнения сценариев: отображение формы записи на курс. 

3. Сценарии заполнения формы записи:

	Входные данные: поля ввода и кнопка отправки данных найдены, отображаются и активны. 
  
    3.1 *Сценарий "Отправка валидных данных"*.
	
		Заполнить поля Имя и Телефон валидными значениями.
		Нажать кнопку "Записаться".
    	Результат выполнения сценария: появляется сообщение об успешной отправке заявки, в БД появляется запись с соответствующими данными.
		
    3.2 *Сценарии "Отправка невалидных данных"*.
	
		3.2.1 "Пустые поля"
		      Оставить все поля пустыми и нажать кнопку "Записаться". 
		      Ожидаемый результат: под всеми полями полявляется сообщение об обязательности их заполнения.
		      
		3.2.2 "Невалидное имя"
		      Заполнить поле Имя невалидным значением. 
		      Заполнить поля Телефон и Эл.почта валидными значениями. 
		      Нажать конопку "Записаться".
		      Ожидаемый результат: под полем Имя появляется соощение с указанием требований к содержанию поля. 
		
		3.2.3 "Невалидный телефон"
              Заполнить поле Телфон невалидным значением. 
              Заполнить поля Имя и Эл.почта валидными значениями. 
              Нажать конопку "Записаться".
              Ожидаемый результат: под полем Телефон появляется соощение с указанием требований к содержанию поля.
              
        3.2.3 "Невалидная Эл.почта"
              Заполнить поле Эл.почта невалидным значением.
              Заполнить поля Имя и Телефон валидными значениями. 
              Нажать конопку "Записаться".
              Ожидаемый результат: под полем Эл.почта появляется соощение с указанием требований к содержанию поля.
        		
    Валидные данные: Виталий, +79876554123, vitaliy@mail.com
    
    Основные варианты невалидных данных для полей:
    
    - *имя*: символы (кроме 1 дефиса), пробелы, цифры
    - *телефон*: буквы, символы, последовательность цифр длиной больше и меньше 11-ти  
    - *эл. почта*: последовательность символов не содержащая `@` и `. + две (минимум) буквы`
	
## Перечень используемых инструментов


**IntelliJ IDEA** - среда разработки программного обеспечения для написания кода

**Java** (версия 11) - язык программирования для написания кода 

**Git** - система контроля версий, позволяет фиксировать изменения в коде, быстро "откатить" изменения назад, сохранять предыдущие версии.

**Gradle/Maven** — система автоматической сборки.

**JUnit-5** - один из самых популярных фреймфорков для модульного тестирования ПО.

**Selenide** - фреймворк для автоматизированного тестирования веб-приложений.

**Lombok** - плагин для автоматической генерации кода, позволяет сократить количество кода.

**Faker** - библиотека для генерации тестовых данных пользователей

## Перечень необходимых разрешений/данных/доступов

* Разрешение на проведение тестирования
* Данные о критериях валидности данных вносимых в поля формы
* Доступ к БД для проверки результата отправки данных

## Перечень и описание возможных рисков при автоматизации

- Неверная оценка трудозатрат на тестирование может привести к увеличению сроков
- Недоступность тестируемого сервиса по техническим причинам может привести увеличение сроков / невозможности тестирования
- Несогласованные изменения тестируемого сервиса может привести к увеличению сроков тестирования

## Перечень необходимых специалистов для автоматизации

QA инженер с опытом автоматизации 

## Интервальная оценка с учётом рисков

Уточнение требований, cогласование и получение разрешений - 2 часа.

Автоматизация 7 сценариев перехода к форме заполнения и минимум 10 тест-кейсов по заполнению формы - 6 часов.

Запас по времени - 2 часа.

Подготовка отчета о тестировании - 2 часа.

Итого - 12 часов.