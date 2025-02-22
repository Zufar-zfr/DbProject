# DbProject



# Система записи к врачу

Веб-приложение для управления записями на прием к врачу. Система позволяет пациентам записываться на прием, а врачам управлять расписанием.

## Функциональность

### Для пациентов
- Выбор даты и времени приема
- Просмотр свободных слотов
- Запись на прием
- Просмотр своих записей

### Для врача
- Просмотр расписания на день
- Блокировка/разблокировка временных слотов
- Управление записями пациентов
- Просмотр статистики

## Технологии

- **Frontend**: HTML, CSS, JavaScript, Bootstrap
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT

## Установка и запуск

1. Клонируйте репозиторий:

2. Установите зависимости

3. Создайте файл `.env` в корневой директории:
env
PORT=3002
MONGODB_URI=mongodb://localhost:27017/appointment-system
JWT_SECRET=your_jwt_secret
4. Запустите MongoDB:
bash
npm run dev

5. Запустите сервер:
bash
npm run dev




## Структура проекта
appointment-system/
├── controllers/
│ ├── appointmentController.js
│ └── authController.js
├── middleware/
│ └── auth.js
├── models/
│ ├── Appointment.js
│ └── User.js
├── routes/
│ ├── appointmentRoutes.js
│ └── authRoutes.js
├── views/
│ ├── appointment.ejs
│ └── doctor-dashboard.ejs
├── .env
├── package.json
└── server.js



## API Endpoints

### Авторизация
- `POST /api/auth/register` - Регистрация нового пользователя
- `POST /api/auth/login` - Вход в систему

### Записи
- `GET /api/appointments/available-times` - Получение доступного времени
- `POST /api/appointments/book` - Создание записи
- `GET /api/appointments/day-schedule` - Получение расписания на день (для врача)
- `POST /api/appointments/block` - Блокировка временного слота (для врача)
- `POST /api/appointments/unblock` - Разблокировка временного слота (для врача)
- `DELETE /api/appointments/:id` - Удаление записи (для врача)
