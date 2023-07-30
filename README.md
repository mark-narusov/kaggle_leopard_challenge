# kaggle_leopard_challenge

Ноутбук для *Kaggle InClass* [соревнования](https://www.kaggle.com/competitions/leopard-challenge-classification/overview) по бинарной классификации для студентов курса [Data Science с Глебом Михайловым](https://stepik.org/course/113596/syllabus).

Задача — предсказать курит человек или нет по его клиническим данным. Целевая метрика — *F1*-мера.

На 30-07-2023 это решение сидит на первом месте на [лидерборде](https://www.kaggle.com/competitions/leopard-challenge-classification/leaderboard).

Используемые алгоритмы и инструменты:
1. *Feature Engineering* с помощью доменных знаний и автоматической генерацией признаков (`sklearn.preprocessing.PolynomialFeatures`).
2. Подбор гиперпараметров случайного леса и градиентного бустинга (*CatBoost*) с помощью *Optuna*.
3. Подбор оптимальных порогов классификации лучших моделей для *F1*-меры.
4. Блендинг предсказаний вероятностей моделей с заданным коэффициентом.
