# RSSHub для Render

Минимальный репозиторий: один `Dockerfile` на базе официального образа [`diygod/rsshub`](https://hub.docker.com/r/diygod/rsshub).

## Деплой на Render

1. Создайте репозиторий на GitHub и запушьте этот проект.
2. В [Render Dashboard](https://dashboard.render.com) → **New** → **Blueprint** (или **Web Service**).
3. **Blueprint**: укажите репозиторий — Render подхватит `render.yaml`.
4. **Web Service вручную**: Runtime **Docker**, Dockerfile path `./Dockerfile`, branch `main`.
5. После деплоя откройте `https://<имя-сервиса>.onrender.com/telegram/channel/<username>` (username канала без `@`).

## Bybit Affiliate

В сервисе `bybit-affiliate` задайте:

```text
TELEGRAM_RSS_URL=https://<имя-сервиса>.onrender.com/telegram/channel/pifagortrade
```

Затем **Синхронизировать** в дашборде.

## Free tier

Инстанс может засыпать без трафика — первый запрос после паузы будет длиннее. При необходимости используйте платный план или внешний cron, пинующий главную страницу.
