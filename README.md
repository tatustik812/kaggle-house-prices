# Kaggle House Prices — Предсказание стоимости недвижимости

## О проекте
Полный ML pipeline для предсказания цены дома на датасете Kaggle House Prices.
Включает EDA, preprocessing и сравнение пока 9 моделей машинного обучения.

## Текущие результаты
| Модель                 | RMSE (log) | RMSE (доллары) |
|------------------------|------------|----------------|
| ElasticNet             | 0.1420     | 25 865.40      |
| Ridge                  | 0.1429     | 25 384.86      |
| Lasso                  | 0.1466     | 28 710.62      |
| Random Forest          | 0.1478     | 31 275.92      |
| Polynomial (degree=2)  | 0.1650     | 31 614.98      |
| Decision Tree          | 0.1920     | 42 196.96      |
| Linear Regression      | 0.2057     | 25 542.57      |
| KNN                    | 0.2076     | 44 173.49      |
| SVR                    | 0.2168     | 45 203.51      |

## Структура проекта
├── 00_EDA.ipynb          # Exploratory Data Analysis
├── 01_Preprocessing.ipynb # Подготовка данных
├── 02_Models.ipynb        # Обучение и сравнение моделей
└── data/

## Стек
Python, pandas, numpy, scikit-learn, matplotlib, seaborn

## Ключевые решения
- Log-трансформация таргета для работы с относительной ошибкой
- Заполнение пропусков через документацию датасета
- GridSearchCV + cross-validation для всех моделей
