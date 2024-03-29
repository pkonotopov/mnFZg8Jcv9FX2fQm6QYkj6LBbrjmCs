# Рабочее окружение для выполнения заданий

### 1. Клонирование репозитория и запуск рабочего окружения

```bash
git clone https://git.postgrespro.ru/p.konotopov/dba-interview.git dba-interview

cd ./dba-interview

docker compose up -d
```

### 2. Соединение с БД `interview`

```bash
docker compose exec postgres psql -U postgres interview
```

### 3. Вывод журналов работы контейнеров

```bash
# вывод состояния контейнеров
docker compose ps -a

# вывод журналов работы
docker compose logs

# вывод журналов работы для избранного контейнера
docker compose logs <имя_контейнера>
```

### 4. Перезапуск стека с переинициализацией БД

```bash
docker compose down

docker volume rm dba_postgres_volume && docker-compose up -d
```

### 5. Соединение с Metabase

В браузере открыть ссылку – [http://localhost:13030](http://localhost:13030)
