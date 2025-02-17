# Pumped-up
Цейзастосунок допомагає користувачам вести облік свого харчування та тренувань, відстежувати кількість спожитих і витрачених калорій, встановлювати особистіцілі та контролювати свій прогрес.
# Проєкт: Онлайн-щоденник харчування та тренувань

## 1. Назва: Pumped up

## 2. Мета
Цей застосунок допомагає користувачам вести облік свого харчування та тренувань, відстежувати кількість спожитих і витрачених калорій, встановлювати особисті цілі та контролювати свій прогрес.

Основні задачі, які вирішує застосунок:
- Ведення щоденника харчування
- Відстеження тренувань
- Контроль споживаних і витрачених калорій
- Встановлення персональних цілей
- Аналіз прогресу та рекомендації

## 3. Користувачі та їх можливості

### Адміністратор
- Додавати/видаляти продукти та вправи
- Керувати користувачами
- Переглядати статистику всіх користувачів

### Звичайний користувач
- Реєстрація та авторизація
- Додавати свої прийоми їжі
- Записувати тренування
- Встановлювати цілі
- Фільтрувати дані за часом, калоріями та типом тренування

## 4. Основні сутності

### User
**Опис:** містить інформацію про зареєстрованого користувача
**Поля:**
- Id (int) – Унікальний ідентифікатор
- Username (string) – Ім'я користувача
- Email (string) – Пошта
- PasswordHash (string) – Хеш пароля
- Role (string) – Роль (admin/user)
- Height (double) – Зріст
- Weight (double) – Вага
- TargetWeight (double) – Бажана вага

### FoodLog
**Опис:** інформація про прийоми їжі
**Поля:**
- Id (int) – Унікальний ідентифікатор
- UserId (int) – Користувач, що додав запис
- FoodName (string) – Назва їжі
- Calories (double) – Кількість калорій
- Date (DateTime) – Дата споживання

### WorkoutLog
**Опис:** запис про тренування
**Поля:**
- Id (int) – Унікальний ідентифікатор
- UserId (int) – Користувач, що додав тренування
- WorkoutType (string) – Тип тренування (біг, силові, йога)
- CaloriesBurned (double) – Витрачені калорії
- Date (DateTime) – Дата тренування

### Goals
**Опис:** запис цілей користувача
**Поля:**
- Id (int) – Унікальний ідентифікатор
- UserId (int) – Користувач, що встановив ціль
- TargetCalories (double) – Ціль по калоріях
- TargetWeight (double) – Цільова вага
- Deadline (DateTime) – Кінцева дата

## 5. Можливості застосунку

| Функція | Опис |
|---------|------|
| Реєстрація та вхід | Користувач може створити акаунт та увійти в систему |
| Додавання харчування | Записати, що він їв, скільки калорій отримав |
| Додавання тренувань | Записати, яке тренування зробив, скільки калорій витратив |
| Встановлення цілей | Вибрати, скільки калорій він хоче споживати, яка у нього цільова вага |
| Перегляд статистики | Візуальний графік споживаних/витрачених калорій |
| Редагування та видалення записів | Можливість виправити або видалити записи харчування і тренувань |
| Фільтрування даних | Фільтри за датою, калоріями, типом тренування |
| Ролі користувачів | Адміністратор керує користувачами та вмістом бази даних |

## 6. Вибір технології UI
- ASP.NET Core MVC + Razor Pages
- Використовуємо Bootstrap для стилізації
- Відображаємо дані у вигляді таблиць та форм
