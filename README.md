
# Тестирование API через Postman

## Цель задания:

Протестировать API платформы (https://blog-platform.kata.academy/api/) с помощью Postman:  
- Зарегистрировать пользователя  
- Выполнить логин  
- Получить данные текущего пользователя через токен авторизации  

## Используемые технологии

- [Postman](https://www.postman.com/) — для отправки HTTP-запросов  
- API-документация: [RealWorld API](https://bump.sh/doc/realworld/operation/operation-createuser)

---

## Запросы:

### 1. Регистрация пользователя

**Метод:** `POST`  
**URL:** `https://blog-platform.kata.academy/api/users`  
**Тело запроса (JSON):**

```json
{
  "user": {
    "username": "mynewuser123",
    "email": "myemail123@example.com",
    "password": "mypassword"
  }
}
```

---

### 2. Логин (авторизация)

**Метод:** `POST`  
**URL:** `https://blog-platform.kata.academy/api/users/login`  
**Тело запроса (JSON):**

```json
{
  "user": {
    "email": "myemail123@example.com",
    "password": "mypassword"
  }
}
```

---

### 3. Получение данных текущего пользователя

**Метод:** `GET`  
**URL:** `https://blog-platform.kata.academy/api/user`  
**Заголовок запроса:**

```
Authorization: Token <мой_токен>
```

Пример:

```
Authorization: Token eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjY4MzM3MTVjNWVmZjZlMWIwMGQyNzQzYiIsInVzZXJuYW1lIjoibXluZXd1c2VyMTIzIiwiZXhwIjoxNzUzMzg1OTc4LCJpYXQiOjE3NDgyMDE5Nzh9.6vpTk1CsQGueW1CfGE5HHnXhSIV1w9HxgTjX_VGUOt4
```

---

## Структура проекта:

```
api-postman.LKY/
├── README.md
└── screenshots/
    ├── registration.png
    ├── login.png
    └── get-user.png
```

---

## Итог:

**Пользователь успешно зарегистрирован, выполнен вход и получены пользовательские данные через авторизацию токеном.  
Все действия протестированы вручную с помощью Postman.  
Скриншоты подтверждают успешное выполнение каждого запроса.**

---

### Задание выполнила:
- **ФИО:** Лакштанкина Кристина  
- **Ник:** KiSS_Ka13L
