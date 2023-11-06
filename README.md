# Дипломный проект. Прогнозирование стоимости жилья для агентства недвижимости.


## Оглавление   
1. Описание проекта
2. Решаемая задача
3. Краткая информация о данных
4. Этапы работы над проектом
5. Результаты
6. Выводы

### 1. Описание проекта    
Разработка и продакшен модели машинного обучения для прогнозирования стоимости объектов недвижимости, выставленных на продажу, с целью увеличения скорости реакции и качества работы риелторов в агентстве недвижимости.  



### 2. Решаемая задача    
Произвести предобработку и разведывательный анализ набора реальных данных рынка недвижимости США, выделить наиболее значимые факторы, влияющие на стоимость недвижимости.  
Построить регрессионную модель для прогнозирования стоимости недвижимости и на ее основе разработать небольшой веб-сервис, на вход которого поступали бы данные о некоторой выставленной на продажу недвижимости, а сервис прогнозировал бы его стоимость.  

**Условия решения задачи:**  
1. Обработать входные данные: пропуски, дубликаты и выбросы, устранить ошибки ввода, расшифровать сокращения.  
2. Провести разведывательный анализ: отыскать закономерности, сгенерировать новые признаки с использованием внешних источников, проиллюстрировать наблюдения и гипотезы с помощью графиков.  
3. Отобрать признаки и подготовить данные для подачи на вход модели.   
4. Обучить несколько моделей регрессии, отобрать лучшую по метрике качества.  

**Метрика качества**     
- Являясь дипломным, проект предоставляет студенту право выбора подходящей метрики качества.  
- Для решении задачи регрессии выбраны метрики: `R2`, `MAPE`, `MAE`.  

**Практикуемые навыки:**     
- предобработка данных;  
- разведывательный анализ;  
- построение диаграмм с помощью библиотеки seaborn и plotly;  
- обучение моделей регрессии;  
- использование алгоритмов оптимизации гиперпараметров RandomizedSearchCV и Optuna;  
- понимание и использование метрик качества моделей.



### 3. Краткая информация о данных  
В датасете представлены 377 тысяч объектов недвижимости, выставленных на продажу. Данные скачаны из системы мультилистинга MLS США и предоставлены менторами Skillfactory.  

Данные реальные, заранее не обработанные, поэтому содержат всевозможные пропуки, дубли, ошибки ввода и проч.  
Информация о признаках датасета приведена в начале ноутбука.  



### 4. Этапы работы над проектом  
1. Знакомство с данными и их предобработка.  
2. Формирование baseline-решения.  
3. Разведывательный анализ данных.  
4. Моделирование и решение задачи регрессии.  


### 5. Результаты  
1. В ходе предобработки данных, выявлены многочисленные пропуски, дубли; намечены шаги для EDA.  
2. На основе предобработанных данных сформировано baseline-решение с использованием модели логистичекой регрессии и CatBostRegressor для последующего сравнения.  
3. Выполнен разведывательный анализ, включавший генерацию новых признаков с помощью десериализации имеющихся и привлечения внешних источников; выдвинуты гипотезы о взаимном влиянии данных; выводы проиллюстрированы диаграммами. 
4. Решена задача регрессии с использованием моделей и алгоритмов: LinearRregression, PolynomialFeatures, DecisionTreeRegressor, RandomForestRegressor, GradientBoostingRegressor, StackingRegressor, CatBoostRegressor, RandomizedSearchCV, Optuna.  
5. На основе сравнения по метрикам качества выбрана модель GradientBoostingRegressor для продакшена.  


### 6. Выводы  
Дипломный проект позволил проверить свои силы и приобретенные за время годового курса DS-знания и навыки на реальной задаче.  

Ввиду необработанных данных удалось в полной мере испытать особености модели CRISP-DM, выполняя прогноз, а затем вновь возвращаясь на этап обработки данных с целью улучшить их и повысить качество моделирования (и так несколько раз!).  

В результате удалось существенно повысить качество моделирования и значения метрик. Так, например, значение целевой метрики `R2` составило 0.69. Дальнейшее их улучшение целиком лежит в плоскости обработки и более глубокого разведывательного анализа входных данных.


