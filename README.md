# Анализ продаж видеоигр в Steam

## Инструменты:

<div>
  <img src="https://img.shields.io/badge/python-white?logo=python&style=for-the-badge" title="Python" alt="Python" height="40"/>&nbsp;
  <img src="https://img.shields.io/badge/pandas-white?logo=pandas&logoColor=blue&style=for-the-badge" title="Pandas" alt="Pandas" height="40"/>&nbsp;
  <img src="https://img.shields.io/badge/numpy-white?logo=numpy&logoColor=black&style=for-the-badge" title="Numpy" alt="Numpy" height="40"/>&nbsp;
  <img src="https://img.shields.io/badge/matplotlib-white?logo=matplotlib&logoColor=black&style=for-the-badge" title="Matplotlib" alt="Matplotlib" height="40"/>&nbsp;
  <img src="https://img.shields.io/badge/seaborn-white?logo=seaborn&logoColor=black&style=for-the-badge" title="Seaborn" alt="Seaborn" height="40"/>&nbsp;
  <img src="https://img.shields.io/badge/re-white?logo=re&logoColor=black&style=for-the-badge" title="Re" alt="Re" height="40"/>&nbsp;
</div>

## Зачем это нужно

Цена, оценки и дата релиза — ключевые факторы, которые могут влиять на продажи игры. В этом проекте я на данных Steam проверил:

- Как цена связана с продажами
- Чьи оценки точнее предсказывают успех: критиков или игроков
- Влияет ли месяц выхода на продажи

Результаты помогают принимать решения по ценообразованию и выбору даты релиза.

---

## Что сделано

- Собраны данные через Steam Spy API и Steam Store API (2407 игр, 8 жанров)
- Проведён исследовательский анализ распределения продаж, цен и оценок
- Из-за ненормального распределения использованы непараметрические тесты (Kruskal-Wallis, Mann-Whitney, Spearman)
- Построены визуализации: графики зависимостей, распределения по жанрам, сезонные паттерны

---

## Ключевые выводы

-  **Цена**  
До $40 повышение цены значимо увеличивает продажи (r = 0.95, p < 0.05). После $40 — дальнейший рост цены не даёт прироста продаж.

- **Оценки**  
Во всех жанрах пользователи оценивают игры выше критиков. Максимальный разрыв — в Indie (+12 баллов), минимальный — в Sports (+4 балла).

-  **Сезонность**  
Месяц релиза значимо влияет на продажи (p < 0.05). Лучшие месяцы — сентябрь и ноябрь, худший — июнь. Осень — наиболее прибыльный сезон для выпуска новых игр.

---

## Ограничения

- Данные собраны через открытые API, продажи оценены косвенно (по количеству отзывов)
- Отсутствуют данные о рекламных бюджетах, себестоимости и чистой прибыли

---



