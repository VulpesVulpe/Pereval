REST API для ФСТР
Реализовал метод submitData для работы с REST запросом формы
submitData нужен только для того, чтобы загружать данные на сервер, сами же данные я предлагаю брать с помощью методов, 
описанных с помощью swagger /swagger GET/POST/PUT/DELETE /perevals возвращает список перевалов с пагинацией /perevals/id возвращает информацию по перевалу, где:

"id":уникальный идентификатор
"beauty_title":название типа
"title":название
"other_titles":третье название
"add_time":время добавления
"status":статус(new, pending, accepted или rejected)
"coords":ссылка на id модели координат /coords/*id*
"level":ссылка на id модели сложности перевала /level/*id*
"images":массив ссылок на картинки перевала с описаниями /images/*id*
"areas":массив ссылок на зоны перевала /areas/*id*

также есть возможность фильтровать перевалы по id создателя и уникальному email создателя с помощью параметров

/perevals/?user_id= & user_email= соответственно
