# ДЗ 4 — DML, DDL та складні SQL-запити

Для цієї роботи я використав **Olist Brazilian E-commerce Public Dataset**: https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

У notebook я завантажую шість CSV: customers, orders, order_items, products, sellers та order_reviews. Дані автоматично отримуються через `kagglehub`, тому для запуску може знадобитися доступ до Kaggle. Використовується повний набір файлів, без навмисного обмеження кількості рядків. Фактичні кількості рядків друкуються після завантаження.

## Як запустити

1. Відкрити `ДЗ3_Смачило_Богдан_Андрійович.ipynb` у Google Colab. https://colab.research.google.com/drive/1gd2NLqAT1tSig-xgUtDnBpSUZZbeBrZw?usp=sharing
2. За потреби налаштувати доступ до Kaggle.
3. Обрати **Runtime → Run all**.
4. Зберегти notebook із результатами виконання.

Notebook встановлює локальний PostgreSQL через `apt-get`, оскільки пакет `pgserver` був недоступний у моєму Colab. Це альтернативний спосіб запуску, який **формально відрізняється від вимоги курсу використовувати `pgserver`**.

## Що зроблено

Я створив raw- та typed-таблиці, налаштував PK/FK/CHECK, перевірив DML-операції з RETURNING та ON CONFLICT, розрахував сегменти покупців за `customer_unique_id`, виконав JOIN-запити, агрегування, INTERSECT і ROW_NUMBER. Пояснення та Reflection додані в notebook.

SQL-запити й повний запуск у Colab потрібно перевірити після завантаження даних. Результати в notebook з'являться після виконання клітинок.
