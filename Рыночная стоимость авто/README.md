## Определение стоимости автомобилей

[HTML](https://github.com/fromufawithlove/Portfolio/blob/main/%D0%A0%D1%8B%D0%BD%D0%BE%D1%87%D0%BD%D0%B0%D1%8F%20%D1%81%D1%82%D0%BE%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%B0%D0%B2%D1%82%D0%BE/AutoPrice.html) [ipynb](https://github.com/fromufawithlove/Portfolio/blob/main/%D0%A0%D1%8B%D0%BD%D0%BE%D1%87%D0%BD%D0%B0%D1%8F%20%D1%81%D1%82%D0%BE%D0%B8%D0%BC%D0%BE%D1%81%D1%82%D1%8C%20%D0%B0%D0%B2%D1%82%D0%BE/AutoPrice.ipynb)

### Описание проекта
Сервис по продаже автомобилей с пробегом «Не бит, не крашен» разрабатывает приложение, чтобы привлечь новых клиентов. В нём можно будет узнать рыночную стоимость своего автомобиля. 
Постройте модель, которая умеет её определять. В вашем распоряжении данные о технических характеристиках, комплектации и ценах других автомобилей.

Критерии, которые важны заказчику:

- качество предсказания;
- время обучения модели;
- время предсказания модели.
  
### Описание данных

Признаки

- DateCrawled — дата скачивания анкеты из базы
- VehicleType — тип автомобильного кузова
- RegistrationYear — год регистрации автомобиля
- Gearbox — тип коробки передач
- Power — мощность (л. с.)
- Model — модель автомобиля
- Kilometer — пробег (км)
- RegistrationMonth — месяц регистрации автомобиля
- FuelType — тип топлива
- Brand — марка автомобиля
- Repaired — была машина в ремонте или нет
- DateCreated — дата создания анкеты
- NumberOfPictures — количество фотографий автомобиля
- PostalCode — почтовый индекс владельца анкеты (пользователя)
- LastSeen — дата последней активности пользователя
  
Целевой признак

- Price — цена (евро)

### Выводы

- Мы обучили 4 вида моделей на предоставленных данных.
- Не все модели показали RMSE < 2500, Линейная Регрессия показала RMSE = 2742,19
- Лучшие показатели RMSE у моделей градиентного бустинга. Они обучаются чуть дольше модели RandomForestRegressor, но дают гораздо большую точность предсказаний.
- Лучший показатель RMSE показала модель CatBoostRegressor. Время обучения больше, чем у RandomForestRegressor, но время предсказаний сравнимо с этой моделью, а точность предсказания выше.
