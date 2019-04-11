# Movie Libary

Одностраничное приложение на ReactJS, с реализацией сервера на Node.js и базой данных MongoDB 

## Структура приложения 
### Клиенсткая часть приложения
```
/client 
 /etc 
 /public
 /src
  /components 
 ```
Клиентская часть приложения реализована на ReactJS и содержится в каталоге ``` /client ```

В подкатологе ``` /public ``` храниться файл ``` index.html ```, который является шаблоном страницы 

В подкатологе ``` /src ``` хранятcя файлы:
  
 - ``` index.js ```, который является точной входа JavaScript  
 
 - ``` App.js ```, который содержит компоненты приложения

Также ``` /src ``` имеет подкаталог ``` /сomponents ``` где храняться стили и компоненты приложения

#### Приложения разбито на такие компоненты: 

  ``` MovieList.js ``` - основной компонент, который отвечает за отображения списка фильмов и остальных компонентов приложения, а так же содержит запросы на сервер 

  ``` Movie.js ``` - компонент для рендеринга карточки фильма, содержит основную информацию про фильм и кнопки просмотра полной информации и удаления 

``` Search.js ``` - компонент для обработки предмета поиска, содержит форму которая возвращает параметры поиска - предмет поиска и фильтр (поиск по имени актера или по названию)

``` SearchError.js ``` - компонент отображения ошибки при поиске фильма 

``` Sort.js ``` - компонент сортировки списка карточек фильма 

``` Adder.js ``` - компонент, содержит кнопку при нажатии на которую, открывается диалоговое окно с формой для добавления нового фильма 

``` Form.js ``` - компонент, который реализует форму добавления нового фильма, возвращает объект для добавления в БД

Стили приложения храняться в папке ``` /scss ```


### Серверная часть приложения 

``` 
/modules 
/routes
index.js 
```

``` index.js ``` - файл запуска сервера. Файл содержит соединение с БД, инициализацию маршрутов, простую обработку ошибок при работе с запросами в БД и запуск сервера. 

Каталог ``` /routers ``` содержит непосредственно REST API реализованный в файле ``` api.js ```. Файл описывает основные маршруты (получение данных, поиск, удаления и сортировку)

Каталог ``` /models ``` содержит файл ``` movie.js ```, в котором храниться схема сохранения записи в БД. 


## Установка и запуск 

``` bash 
#Установка зависимостей для сервера 
npm install 

#Установка зависимостей для клиентской части 
npm run client-install

#Запуск одновременно сервера и клиентской части 
npm run dev

#Запуск только серверной части (http://localhost:4000)
npm run server 

#Запуск только клиентской части (http://localhost:3000)
npm run client

```
