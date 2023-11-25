# Предугадывание оттока клиентов в Burger King
*** 

### Задача
***
По дата-сету нужно составить предугадывание оттока клиентов и количества дней, через которое они могут уйти. 

### Описание данных 
***
Формат сабмита:

csv файл с колонками: customer_id, date_diff_post, buy_post
один customer_id - одна запись в сабмите (совершит ли этот клиент транзакцию в течение 60ти дней с момента последней известной транзакции, и если да, то через сколько дней)
Сабмит грузится на платформу в csv файле разделитель ;



### Описание полей 
***
- `customer_id` — идентификатор клиента
- `group_name` — группа (test или train)
- `revenue` — доход с позиции из корзины
- `startdatetime` — Дата и время продажи
- `dish_name` — название блюда
- `ownareaall_sqm` — площадь ресторана
- `format_name` — формат ресторана
- `buy_post`  —Таргет 1: флаг оттока (0 – отток, 1 – не отток)
- `date_diff_post` — Таргет 2: количество дней между последней покупкой в прошлом и первой в будущем, только в train данных

### Использование  
***

- `RFM.ipynb` - подсчет rfm по пользователю и торговой точке
- `current_aggregations.ipynb` - считаются простые агрегации 
- `embedings.ipynb` - просчет эмбедингов LaBSE - https://huggingface.co/cointegrated/LaBSE-en-ru
- `predict_cat_boost_datasphere-2.ipynb` - классификатор 
- `Model_RMSE.ipynb` - 



### Итоги 
***
Наша изначальная задача выполнена с результатов `f1` равным 0.67 и `AUC-ROC` равным 0.71 , а бОльшим набором данным данная метрика может быть значительно улучшено.

Данное решение можно будет использовать для масштабирования на 

### Используемые библиотеки 
***
- `pandas`
- `numpy`
- `matplotlib`
- `sklearn`
- `

