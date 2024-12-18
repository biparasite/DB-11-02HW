# Домашнее задание к занятию " `Кеширование Redis/memcached` " - `Сулименков Алексей`

---

## Задание 1. Кеширование

Приведите примеры проблем, которые может решить кеширование.

### Ответ

Основная функция кэша – ускорение процесса извлечения данных. Он избавляет от необходимости обращаться к менее скоростному базовому уровню хранения, что влияет на увеличение пропускную способность, экономии ресурсов, а также повышение производительность приложений.

---

## Задание 2. Memcached

Установите и запустите memcached.

Приведите скриншот systemctl status memcached, где будет видно, что memcached запущен.

### Ответ

![Memcached status](https://github.com/biparasite/DB-11-02HW/blob/main/memcached_status.png)

---

## Задание 3. Удаление по TTL в Memcached

Запишите в memcached несколько ключей с любыми именами и значениями, для которых выставлен TTL 5.

Приведите скриншот, на котором видно, что спустя 5 секунд ключи удалились из базы.

### Ответ

Команды для установки ttl = 5, для сохранения 5 байт

```memcached
set name 0 5 5
test1
```

Проверка, что данные удалены через заданный ttl

```memcached
set test1
```

Скриншот
![Memcached ttl](https://github.com/biparasite/DB-11-02HW/blob/main/memcached_ttl.png)

---

## Задание 4. Запись данных в Redis

Запишите в Redis несколько ключей с любыми именами и значениями.

Через redis-cli достаньте все записанные ключи и значения из базы, приведите скриншот этой операции.

### Ответ

Запись в redis ключа и значаения с бесконечным ttl

```redis
set test1 test1
```

Извлечение по ключу

```redis
get test1
```

Скриншот
![Redis](https://github.com/biparasite/DB-11-02HW/blob/main/redis.png)

---

## Задание 5\*. Работа с числами

Запишите в Redis ключ key5 со значением типа "int" равным числу 5. Увеличьте его на 5, чтобы в итоге в значении лежало число 10.
Приведите скриншот, где будут проделаны все операции и будет видно, что значение key5 стало равно 10.

### Ответ

![Redis](https://github.com/biparasite/DB-11-02HW/blob/main/redis_incrby.png)
