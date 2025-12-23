# LR: Docker + Flask + Redis (Dockerfile + Docker Compose)

Небольшое веб-приложение на **Flask**, которое хранит счётчик посещений в **Redis**.  
Запуск выполняется через **Docker Compose** (2 контейнера: `web` и `redis`).

---

## Стек
- Python (Flask)
- Redis
- Docker / Docker Compose

---

## Структура проекта
```txt
hello-docker/
  app.py
  requirements.txt
  Dockerfile
  docker-compose.yml
  screenshot/
    This page has been viewed 1 times..png
    This page has been viewed 2 times..png
  README.md
````

---

## Запуск

В корне проекта (где лежит `docker-compose.yml`):

```bash
docker compose up --build
```

Открыть в браузере:

* [http://127.0.0.1:5000](http://127.0.0.1:5000)

При обновлении страницы счётчик должен увеличиваться.

---

## Остановка

```bash
docker compose down
```

---

## Результат (скриншоты)

**1 просмотр:**
screenshot/This page has been viewed 1 times..png

**2 просмотра:**
screenshot/This page has been viewed 2 times..png

---

## Висновок

У ході лабораторної роботи було створено багатоконтейнерний застосунок Flask + Redis та розгорнуто його за допомогою Docker Compose. Було підготовлено Dockerfile для складання образу веб-сервісу, встановлено залежності та налаштовано запуск двох сервісів (web і redis). Після запуску застосунку перевірено роботу лічильника переглядів у браузері — значення збільшується при оновленні сторінки, що підтверджує коректну взаємодію з Redis. Отримані навички дозволяють швидко збирати та запускати подібні мікросервісні застосунки у контейнерах.

```

Если хочешь — могу ещё добавить маленький блок **“Як працює”** (2–3 строки) или **“Параметри”** (про `APP_PORT`).
```
