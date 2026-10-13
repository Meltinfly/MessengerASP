# 🏣 Корпоративный мессенджер

[![.NET](https://img.shields.io/badge/.NET_9.0-purple?style=for-the-badge&logo=.net)](https://dotnet.microsoft.com/en-us/download/dotnet/9.0)
[![MS_SQL Server](https://img.shields.io/badge/MS_SQL_Server-2022-orange?style=for-the-badge&)](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)
[![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/get-started)
[![Docker Compose](https://img.shields.io/badge/Docker%20Compose-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://docs.docker.com/compose/install/)

**CorpNetMessenger** — это внутренний корпоративный мессенджер, который позволяет сотрудникам компании обмениваться текстовыми сообщениями и файлами в режиме реального времени.

## 🚀 Быстрый запуск (за 3 команды)

Проект полностью готов к запуску через Docker Compose:

### 🔧 Перед запуском

Убедитесь, что на вашем компьютере установлены:

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

### ▶️ Запуск приложения

1. Клонируйте репозиторий:

```bash
git clone https://github.com/Meltinfly/MessengerASP.git
cd MessengerASP
```

2. Скопировать файл окружения:

```bash
cp .env.example .env
```

3. Запустите приложение с помощью Docker Compose:

```bash
docker compose up --build
```

4. После запуска приложение будет доступно по адресу:
   http://localhost:8080

### 👤 Тестовые пользователи

При первом запуске в системе создаются два тестовых пользователя:

- Администратор:
  - Логин: admin
  - Пароль: 123456
- Обычный пользователь:
  - Логин: user
  - Пароль: 123456

Используйте эти учетные данные для входа в систему после развертывания.

## 📋 Основные функции:

- Обмен текстовыми сообщениями
- Отправка и получение файлов
- Авторизация и аутентификация пользователей
- Работа в группах/комнатах
- История переписки

## 🛠️ Технологии

| Категория     | Технология                          |
| ------------- | ----------------------------------- |
| Backend       | ASP.NET Core 9                      |
| База данных   | MS SQL Server                       |
| ORM           | Entity Framework Core (Code First)  |
| Фронтенд      | HTML/CSS/JavaScript/Bootstrap       |
| Дополнительно | SignalR для чата в реальном времени |

---

## 🗃️ Структура проекта

```
📦 CorpNetMessenger/
├── 📂 Domain/                      # Доменные модели и интерфейсы
│   ├── 📂 DTOs/                    # Data Transfer Objects (чистые модели данных)
│   ├── 📂 Entities/                # ORM-сущности
│   ├── 📂 Interfaces/              # Сервисные интерфейсы
│   └── 📂 MappingProfiles/         # Профили AutoMapper
│
├── 📂 Application/                 # Основная логика приложения (слой приложения)
│   ├── 📂 Common/                  # Общие компоненты
│   ├── 📂 Converters/              # Конвертеры для преобразования данных
│   └── 📂 ValidationAttributes/    # Кастомные атрибуты валидации
│
├── 📂 Infrastructure/              # Реализация репозиториев и сервисов
│   ├── 📂 Data/                    # Контекст EF + миграции
│   ├── 📂 Repositories/            # Работа с БД
│   └── 📂 Services/                # Бизнес-логика
│
├── 📂 Web/                         # Веб-слои
│   ├── 📂 Areas/                   # Логические разделы (Admin, Messaging)
│   ├── 📂 Controllers/             # MVC контроллеры
│   ├── 📂 Hubs/                    # SignalR хабы
│   ├── 📂 ViewModels/              # Модели представления
│   └── 📂 Views/                   # Razor-шаблоны
└── Program.cs                      # Точка входа
```

## 📸 Скриншоты

### Авторизация

<img src="assets/screenshots/Login.png" width="500">

### Регистрация

<img src="assets/screenshots/Registration.png" width="500">

### Чат

<img src="assets/screenshots/Chat.png" width="500">

### Увеличенное изображение

<img src="assets/screenshots/Enlarged_image.png" width="500">

### Информация о сотрудниках

<img src="assets/screenshots/Employee_info.png" width="500">

### Редактирование профиля

<img src="assets/screenshots/Profile-editer.png" width="500">

### Запросы на регистрацию (Админ-панель)

<img src="assets/screenshots/Requests.png" width="500">

## 📬 Связь

Если у вас есть вопросы или предложения, напишите мне:

- Email: mihaylov.slava@outlook.com
- Telegram: @Fl1cker_0
