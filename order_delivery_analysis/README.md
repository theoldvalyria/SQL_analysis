# Анализ данных e-commerce и доставки продуктов - SQL код

## Описание

Проект включает анализ данных (SQL Код) в области электронной коммерции и доставки. Основная цель — извлечь ценные инсайты из данных о заказах и деятельности курьеров, чтобы улучшить бизнес-процессы и оптимизировать работу платформы. 

В рамках проекта проведён комплексный анализ, включая расчёт ежедневной выручки, оценку работы курьеров, изучение времени между заказами и их доли в общей выручке. Также осуществлена замена идентификаторов товаров на наименования и определение средней стоимости товаров. Проект позволяет выявить ключевые тренды и улучшить стратегическое планирование.

## Инструменты
`PostgreSQL`  `Windows` `Subqueries`  `CTE`

## Структура таблиц
<img src="https://storage.yandexcloud.net/klms-public/production/learning-content/152/1762/17923/51794/244290/2023_01_24_214337_negate.jpg" alt="Alt text" width="520"> 

## Решенные задачи

1. **Формирование таблицы с датами рождения и числом пользователей/курьеров**

2. **Определение показателей для пользователей:**
   - Рассчитаны общее число заказов, среднее количество товаров в заказе, суммарная стоимость покупок, средняя стоимость заказа, минимальная и максимальная стоимость заказа.

3. **Анализ ежедневной выручки сервиса:**
   - Рассчитана ежедневная выручка на основе данных из таблиц `orders`, `products`, и `user_actions`.

4. **Топ-10% курьеров по количеству заказов:**
   - Определены топ-10% курьеров по количеству доставленных заказов, выведены `id` курьеров, количество доставленных заказов и порядковый номер.

5. **Анализ первых и повторных заказов:**
   - Рассчитано количество первых и повторных заказов на каждую дату и доля первых и повторных заказов.

6. **Замена ID товаров на наименования:**
   - Заменены списки с `id` товаров на наименования товаров и добавлена колонка `product_names`.

7. **Средняя цена товаров:**
   - Рассчитана средняя цена всех товаров и средняя цена без учёта самого дорогого товара.

8. **Накопительные суммы заказов и отмен:**
   - Рассчитаны накопительные суммы оформленных и отменённых заказов и рассчитан показатель `cancel_rate`.

9. **Выбор курьеров с 10 и более днями работы:**
   - Отобраны курьеры, работающие 10 и более дней, и подсчитано количество доставленных заказов.

10. **Стоимость каждого заказа и доля в ежедневной выручке:**
    - Рассчитана стоимость каждого заказа, ежедневная выручка и доля стоимости заказа в ежедневной выручке.

11. **Ежедневный прирост выручки:**
    - Рассчитан ежедневный прирост выручки в абсолютных значениях и в процентах относительно предыдущего дня.

12. **Порядковый номер заказов и время между заказами:**
    - Рассчитан порядковый номер каждого заказа для пользователей, а также время, прошедшее с момента предыдущего заказа.

13. **Доля стоимости заказа в ежедневной выручке:**
    - Рассчитана доля стоимости каждого заказа в ежедневной выручке, выраженная в процентах.

14. **Скользящее среднее числа заказов:**
    - Рассчитано скользящее среднее числа заказов с использованием данных за три предыдущих дня.

15. **Курьеры, доставляющие больше заказов, чем в среднем:**
    - Отмечены курьеры, которые доставили больше заказов, чем в среднем по компании, с помощью `CASE`.

16. **Порядковый номер курьеров по количеству заказов:**
    - Выведены топ 10% курьеров по количеству заказов с порядковым номером в зависимости от числа доставленных заказов.

17. **Среднее время между заказами:**
    - Рассчитано среднее время между заказами для пользователей, оформивших более одного неотменённого заказа.

18. **Прирост выручки по дням:**
    - Рассчитан прирост выручки по дням как в абсолютных значениях, так и в процентах.

