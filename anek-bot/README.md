**Описание**

Бот для [ чата Радио-Т](https://chat.radio-t.com/)

Подгружает список анекдотов по разным темам из RSS сайта anekdot.ru

Реагирует на фразы в которой есть слова 'расскажи' и 'анекдот', отвечая анекдотом из основного списка (про программистов )

Также знает несколько дополнительных тем:
+ интернет
+ твиттер
+ Гейтс
+ iphone

На запрос 'расскажи анекдот про твиттер', ответит анекдотом про твиттер

**Структура проекта**

Папка `app` - В эту папку траншпилируется исходники из TypeScript (TS) в JavaScript

Папка `src` - Исходники на TS

Папка `typings` - Определения необходимые TS для работы с JS библиотеками

`tsconfig.json` - настройки компилятора TS

`typings.json` - настройки утилиты [typings](https://github.com/typings/typings) 
 

Для тестирования `curl`-ом нужно указать `content-type`
```
curl \
     -v \
     -X POST \
     -d '{"text":"Расскажи анекдот","username":123,"display_name":"login"}' \
     -H 'content-type:application/json'   http://192.168.0.30:8080/
```