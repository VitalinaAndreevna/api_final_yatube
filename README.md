# Проект API для Yatube
Проект от Яндекс.Практикум в виде социальной сети, в которой есть публикации, комментарии, группы и подписки.
Автор: Ерохина Виталина Андреевна

# Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/VitalinaAndreevna/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv .venv
```

```
source .venv/bin/activate
```

Установить зависимости из файла requirements.txt:

```
python -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```

Выполнить миграции:

```
python manage.py migrate
```

Запустить проект:

```
python manage.py runserver
```

# Примеры запросов к API:

- Публикация поста
```
POST /api/v1/posts/
{
    "text": "string"
}
```

- Получение постов постранично
```
GET /api/v1/posts/?limit=10&offset=10
```

- Получение определенного поста
```
GET /api/v1/posts/{post_id}/
```

- Получение всех комменатриев определенного поста

```
GET /api/v1/posts/{post_id}/comments/
```

- Удаление комментария

```
DEL /api/v1/posts/{post_id}/comments/{comment_id}/
```
