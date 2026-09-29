# AI-CO Gantt — Firebase версия

## Первый вход
Откройте сайт и введите:

admin@yandex-team.ru

Если база пустая, приложение само создаст этого пользователя с ролью `admin` и загрузит стартовые задачи в `/tasks`.

## Роли
- admin — редактирует задачи и управляет доступами;
- editor — редактирует задачи;
- viewer — только смотрит.

Администратор нажимает **Доступы** и сам добавляет корпоративные почты и роли.

## Деплой
1. Загрузите `index.html` и `vercel.json` в GitHub-репозиторий.
2. Подключите репозиторий к Vercel.
3. Framework preset: Other.
4. Build command не нужен.
5. После деплоя всем можно давать одну постоянную ссылку.

## Firebase
Подключено к:
gantt-control-center-default-rtdb.europe-west1.firebasedatabase.app

Важно: вход по одной почте — это внутренний client-side gate, а не криптографическая аутентификация.
При такой схеме Firebase Realtime Database Rules не могут надёжно различать admin/editor/viewer.
