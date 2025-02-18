# **Разработка сервиса для создания и управления персонализированными плейлистами на YouTube**

**Описание проекта:**
Создать веб-приложение, позволяющее пользователям авторизоваться, создавать персональные плейлисты на YouTube, скачивать видео и управлять ими.

---

## **Функциональные требования:**

### **Регистрация и авторизация пользователей**

- Реализовать регистрацию с подтверждением по email.
- Возможность входа через учетную запись (JWT или session-based).

---

### **Работа с видео**

- Пользователь может добавлять ссылки на видео с YouTube для добавления в плейлисты.
- Доступна загрузка видео с использованием yt_dlp с выбором качества и формата.
- Валидация ссылок: обработка ошибок при вводе недействительных ссылок.

---

### **Создание и управление плейлистами**

- Пользователь может создавать, редактировать и удалять плейлисты.
- Плейлисты должны храниться в базе данных PostgreSQL.
- Возможность сортировки и поиска по плейлистам.

---

### **API для интеграции**

- Разработать REST API для управления плейлистами и скачивания видео.
- Предусмотреть защиту маршрутов (только авторизованные пользователи).

---

### **Фронтенд**

- Простой интерфейс для работы с приложением (можно использовать Django templates).
- Страницы: главная, авторизация, управление плейлистами.

---

### **Логирование и мониторинг**

- Вести логирование операций скачивания и работы с плейлистами.
- Создать админ-панель для просмотра статистики (Django Admin).

---

## **Технические требования:**

### **Backend:**

- Django для логики и API.
- PostgreSQL для хранения данных.

### **Frontend:**

- Django Templates (или любой другой минимальный фронтенд).

### **NGINX:**

- Настроить NGINX как обратный прокси для перенаправления запросов к backend.
- Обеспечить защиту от несанкционированного доступа и эффективную обработку статики.

## **Docker:**

- Контейнеризация всех компонентов: Django, PostgreSQL, NGINX.
- Настроить docker-compose для запуска всех сервисов одной командой.
- Обеспечить изоляцию окружений (production и development).

## **Дополнительно:*

- Использовать .env файлы для управления конфигурацией.
- Реализовать деплой локально или на сервере с помощью Docker.