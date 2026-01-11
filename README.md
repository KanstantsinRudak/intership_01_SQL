# SQL & PostgreSQL для стажёров WhiteSnake

Добро пожаловать! Этот репозиторий создан для стажёров компании WhiteSnake. Здесь вы сможете шаг за шагом освоить основы работы с базами данных и научиться применять знания в реальных задачах.

---

## Содержание

- [Что вы найдёте внутри](#что-вы-найдёте-внутри)
- [Теория](#теория)
- [Практика](#практика)
- [Нормальные формы](#нормальные-формы)
- [Индексы](#индексы)
- [Продвинутый уровень](#продвинутый-уровень-опционально)

---

## Что вы найдёте внутри

| Раздел | Описание |
|--------|----------|
| Основы SQL | Первые запросы, работа с таблицами, объединения и агрегаты |
| PostgreSQL | Особенности СУБД, настройка окружения, базовые команды администрирования |
| Индексы и оптимизация | Зачем нужны индексы, какие бывают, как ускорять запросы |
| Нормальные формы | Простое объяснение нормализации и примеры из практики |
| Учебные материалы | Конспекты, ссылки на курсы и статьи |
| Практика | Задания для тренировки и разбор типичных кейсов |

---

## Теория

### Интерактивные курсы

- [Симулятор SQL от Карпов.Курсы](https://karpov.courses/simulator-sql) — интерактивный тренажёр для изучения SQL с нуля, пошаговые уроки с практикой на реальных данных
- [SQL Tutorial — DataLemur](https://datalemur.com/sql-tutorial) — краткая теория по SQL с примерами, подходит для повторения и подготовки к собеседованиям

### Книги

- [PostgreSQL. Основы языка SQL](./BOOKS/PostgreSQL.%20Основы%20языка%20SQL.pdf) — базовый учебник по SQL в контексте PostgreSQL, рекомендуется для первого знакомства
- [Оптимизация запросов в PostgreSQL (2022, Домбровская)](./BOOKS/Optimizatsia_Zaprosov_V_PostgreSQL_2022_Dombpovckaya.pdf) — для тех, кто хочет писать быстрые запросы

### Видеоматериалы

- [Вопросы с собеседований по SQL](https://www.youtube.com/playlist?list=PLqAk2mIiDakkhP7ooRfS9BBfYfIzHa688) — плейлист с разбором популярных тем: типы данных, оконные функции, виды JOIN (физические и логические), особенности NULL, отличия TRUNCATE/DELETE/DROP, EXPLAIN, VACUUM

---

## Практика

### Тренажёры

| Платформа | Описание |
|-----------|----------|
| [SQL-EX](https://sql-ex.ru/) | Классический тренажёр с большим количеством задач разной сложности |
| [LeetCode: Top SQL 50](https://leetcode.com/studyplan/top-sql-50/) | Базовый набор из 50 задач, обязательный минимум |
| [LeetCode: Расширенный SQL (50 + 27)](https://leetcode.com/problem-list/m8baczxh/) | Базовые 50 задач + 27 дополнительных для углублённой практики |
| [DataLemur](https://datalemur.com/questions) | Около 50 задач на SQL и 40 на Python, реальные вопросы с собеседований |

Рекомендуемый порядок: SQL-EX → LeetCode Top 50 → LeetCode Extended → DataLemur

---

## Нормальные формы

Нормализация — процесс организации данных в базе для уменьшения избыточности и предотвращения аномалий. Обязательная тема для понимания проектирования БД.

### Теория

- [1-3 нормальные формы](https://www.youtube.com/watch?v=zwQzL80U51c) — видео с разбором базовых нормальных форм
- [НФ Бойса-Кодда, 4 и 5 НФ](https://www.youtube.com/watch?v=y5MeJ3bc-OA) — продолжение, более строгие формы
- [Нормальные формы БД](https://habr.com/ru/articles/254773/) — статья для справки, можно использовать как шпаргалку

### Практика

- [Практикум по нормальным формам](./BOOKS/normal_tables.pdf) — задания на приведение таблиц к нормальным формам

---

## Индексы

- [Индексы и партиционирование](./INDEXES_AND_PARTITIONS/README.md) — локальный конспект
- [B-tree индексы](https://habr.com/ru/companies/quadcode/articles/696498/) — разбор самого популярного типа индексов
- [Hash индексы](https://habr.com/ru/companies/otus/articles/814537/) — когда hash лучше B-tree и в чём ограничения

---

## Продвинутый уровень (опционально)

Этот раздел для тех, кто хочет глубже понять внутреннее устройство PostgreSQL.

### Изоляция и многоверсионность (MVCC)

Цикл статей от PostgresPro о параллельной работе транзакций:

1. [Изоляция: как её понимают стандарт и PostgreSQL](https://habr.com/ru/companies/postgrespro/articles/442804/)
2. [Слои, файлы, страницы — физический уровень](https://habr.com/ru/companies/postgrespro/articles/444536/)
3. [Версии строк, виртуальные и вложенные транзакции](https://habr.com/ru/companies/postgrespro/articles/445820/)
4. [Снимки данных и видимость версий строк](https://habr.com/ru/companies/postgrespro/articles/446652/)
5. [Внутристраничная очистка и HOT-обновления](https://habr.com/ru/companies/postgrespro/articles/449704/)
6. [Обычная очистка (VACUUM)](https://habr.com/ru/companies/postgrespro/articles/452320/)
7. [Автоматическая очистка (autovacuum)](https://habr.com/ru/companies/postgrespro/articles/452762/)
8. [Переполнение счётчика транзакций и заморозка](https://habr.com/ru/companies/postgrespro/articles/455590/)

### Журналирование (WAL)

Как PostgreSQL обеспечивает надёжность и восстановление после сбоев:

1. [Буферный кеш](https://habr.com/ru/companies/postgrespro/articles/458186/)
2. [Журнал предзаписи (WAL) — устройство и восстановление](https://habr.com/ru/companies/postgrespro/articles/459250/)
3. [Контрольная точка и фоновая запись](https://habr.com/ru/companies/postgrespro/articles/460423/)
4. [Настройка журнала — уровни, надёжность, производительность](https://habr.com/ru/companies/postgrespro/articles/461523/)

### Блокировки

Механизмы блокировок для обеспечения согласованности данных:

1. [Блокировки отношений (таблиц)](https://habr.com/ru/companies/postgrespro/articles/462877/)
2. [Блокировки строк](https://habr.com/ru/companies/postgrespro/articles/463819/)
3. [Блокировки других объектов и предикатные блокировки](https://habr.com/ru/companies/postgrespro/articles/465263/)
4. [Блокировки в оперативной памяти](https://habr.com/ru/companies/postgrespro/articles/466199/)

### Индексы: глубокое погружение

Полный цикл статей от PostgresPro о всех типах индексов:

1. [Введение](https://habr.com/ru/companies/postgrespro/articles/326096/)
2. [Классы и семейства операторов](https://habr.com/ru/companies/postgrespro/articles/326106/)
3. [Hash-индексы](https://habr.com/ru/companies/postgrespro/articles/328280/)
4. [B-tree](https://habr.com/ru/companies/postgrespro/articles/330544/)
5. [GiST, R-tree, RD-tree](https://habr.com/ru/companies/postgrespro/articles/333878/)
6. [SP-GiST](https://habr.com/ru/companies/postgrespro/articles/337502/)
7. [GIN](https://habr.com/ru/companies/postgrespro/articles/340978/)
8. [RUM](https://habr.com/ru/companies/postgrespro/articles/343488/)
9. [BRIN](https://habr.com/ru/companies/postgrespro/articles/346460/)
10. [Bloom](https://habr.com/ru/companies/postgrespro/articles/349224/)

---

Удачи в изучении.

Команда WhiteSnake 🐍