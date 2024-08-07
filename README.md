# Автоматизирование тестирование веб-приложения с помощью программы Lexema-RPA Studio
## Подготовка окружения
В данном репозитории хранятся исходные файлы автотестов.

**Внимание!** Необходимо скачать файлы в формате rpa и xls (поместите их на **рабочий стол**);

В файле формата xls заполняются: сайт на который необходимо перейти, логин и пароль для авторизации. Также там хранятся исходные данные для подставления ФИО, должностей и т.д;

**Чтобы скачать автотесты нужно:**
1. Выбрать любую папку для сохранения на вашем компьютере
2. В выбранной папке нажать правую клавишу мыши и выбрать Git Bash Here
3. Прописать команду `https://github.com/AutoTestLexema/AutoTestRPA.git` и нажать Enter
4. Дождаться пока скачается данный репозиторий

Для запуска необходимо:
* Скачать Lexema-RPA Studio по [ссылке](https://www.lexema.ru/solutions/lexema-rpa-programmnye-roboty/lexema-rpa-studio/);
### Авторизация Lexema-RPA Studio
1. Запустите программу;
4. Пройдите авторизацию;

## Запуск автотеста:
* В панели инструментов выберите: **Открыть проект**
![image](https://user-images.githubusercontent.com/107256556/174528063-a7aee815-bf47-47e7-b97c-ab2c45cc0207.png)
* Выберите файл в формате rpa и нажмите **Открыть**
* Нажмите два раза по модулю Excel 
![image](https://user-images.githubusercontent.com/107256556/174528369-bb56120e-ba5f-431d-810a-65439a3ea6b7.png)
* Проверьте что путь к файлу Excel, который вы скачали из репозитория, верный. Нажмите на открыть папку, выберите файл Excel и нажмите **Сохранить**
![image](https://user-images.githubusercontent.com/107256556/174529114-47d90a43-d063-4920-b0a2-37dcd1857b6f.png)
* После загрузки файла в проект, нажмите кнопку **Запустить робота**;

![image](https://user-images.githubusercontent.com/107256556/174530607-614a141e-a94d-4397-a846-093c7788f59f.png)

Автотестирование проходит в автоматическом режиме. **Настоятельно рекомендуется не вмешиваться в работу робота**


## Примечание
При неправильной работе робота будет уведомление о том что скрипт сработал с ошибкой; напротив модуля, который сработал неправильно будет красный крестик, и в выводах красным что именно не сработало
![image](https://user-images.githubusercontent.com/107256556/174529582-4346bd73-1e67-4d34-bfae-5dadc9bba252.png)

## Нахождение файла с логами программы
Программа пишет все логи в файл, находящийся в папке %tmp% \ Lexema-RPA \ .... \ .... (.... - название папки в формате год-месяц-день, например **2022-6-20**, когда был запущен робот). Непосредственно внутри программы идут только поверхностные логи, те, что внизу экрана. 

## Вопрос - ответ
В: - "Ошибка в действии Считать данные, сообщение об ошибке - Ссылка на объект не указывает на экземпляр объекта."

О: - Неверно указан путь к файлу в модуле. Зайдите в модуль, который не сработал, и проверьте путь к файлу

В: - "Timed out after 5 seconds"

О: - Прошел таймаут, в течение которого робот не смог выполнить нужное действие. Увеличьте таймаут в модуле.

По другим вопросам работы пишите в [телеграм](https://t.me/AutoTest_Lexema)
