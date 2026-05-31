Хакатон: ChemAI: Predict the Cure
Команда: team17
Результат: ~265.38 (RMSE)

Коротко о решении

Мы предсказываем три таргета: IC50, CC50, SI.
Основная идея: ансамбль baseline + донор с калибровкой.

Финальная формула:
donor = 0.475 × fast_kfold + 0.525 × fast_group

IC50 = baseline + 1.675 × (donor − baseline)
CC50 = baseline + 0.925 × (donor − baseline)
SI   = baseline (без калибровки)

Структура репозитория:
265practice_refactor.ipynb  # основной ноутбук с решением
train.csv                   # данные
test.csv                    # данные
README.md                   # этот файл

Как запустить
Положите train.csv и test.csv в папку с ноутбуком.
Откройте 265practice_refactor.ipynb в Jupyter.
Запустите все ячейки по порядку.
На выходе получите submission.csv.