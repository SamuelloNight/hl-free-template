## HL Free Template

> Это бесплатный шаблон главной страницы сайта для игрового 
сервера **Counter-Strike: Source** и **Counter-Strike: Global Offensive**.

> ![Alt-текст](https://i.ibb.co/84JfFZY/hl-free-tempate.jpg)  


## Настройка
> Весь контент сайта редактируется в файле **appdata.json**.  

**Как изменить меню сайта?**  
Для этого нужно изменить секцию **navigation** в **appdata.json**.  

**"text":** Отображаемый текст  
**"link":** Ссылка куда она введёт  
**"is_spa":** Принимает 2 значения, true или false. Устанавливайте false эта ссылка на сторонний ресурс или на другой каталог сайта. Например: www.example.com/sourcebans  
```json
  {
    "text": "Статистика",
    "link": "/statistics",
    "is_spa": true
  }
```

**Как добавить сервер в мониторинг?**  
Для этого нужно изменить секцию **servers** в **appdata.json**.  

**"platform":** Платформа на котором работает сервер. Принимает только значение "css" и "csgo"  
**"address":** IP адрес сервера  
```json
  {
    "platform": "css",
    "address": "46.174.53.82:27015"
  }
```

> Все остальные данные можно изменить там же.  


## Выгрузака сайта на хостинг

**1.** Скачайте шаблон нажав не зеленую кнопку **"Code"** в начале документа.  
**2.** Перекиньте файлы в корневой каталог сайта.  


## Используемый стэк

**1. PHP** &ndash; Язык программирования для серверной части.  
**2. SASS** &ndash; Препроцессор для CSS.  
**3. VueJS** &ndash; JavaScript фреймворк.  
**4. Axios** &ndash; JS библиотека для отправки асинхронных запросов на сервер.  
**5. Bootstrap** &ndash; CSS фреймворк (используется только для сброса стилей и сетка).  
**6. LaravelMix** &ndash; Сборщик для FrontEnd основанный на WebPack.  

## Редактирование шаблона

> Для редактирования шаблона, вам нужны хотябы базовые знания JavaScript. 
Вся разметка и стили редактируются в компонентах **Vue** по пути ``"resources/js/components"``.
Для того чтобы применить изменения, вам нужен [NodeJS](https://nodejs.org/ru/). 
После установки, выполните следующие действия:

**1.** Перейдите в корневую папку с проектом  
**2.** Запустите команду ``npm install``  
**3.** Запустите команду ``npm run prod``  
**4.** Замените файлы **index.js** и **index.css** в папках ``"public/js"`` и ``"public/css"`` на хостинге.
