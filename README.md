# Data analysis
___
### Анализ и обработка датасета для ML
    Задание phase0 в elbrus bootcamp
В рамках данной задачи необходимо подготовить dataset для обучения на основе ~~плохого~~ dataframe, сформированного на основе более 20 тыс. объявлений об аренде недвижимости на <u>cian.ru</u> 
    Последовательность работы над dataframe:
1) Из предложенного *dataset* была совершена выборка по интересующему городу.
2) Существующие данные приводим к формату, удобного для последующего обучения согласно ТЗ, а именно:
   * Комнатность и площадь квартиры задаётся одним числом
   * *NaN* в *окна, ремонт, мусоропровод и др.* меняем согласно логики
   * Избавляемся от NaN для лифтов, если меньше 5 этажей - нет лифта, в остальном по одному каждого лифта
   * *NaN* в *Дополнительно* заменяем на *пусто*. Данная колонка понадобится для последующего анализа
   * Расстояние до метро, заданное в формате "пеш./маш. время" переводим в расстояние в м согласно
   >    Человек за минуту проходит 70 м, машина 750 м.
3) Удаляем неинформативные в рамках текущего заданния колонки, проверяем на наличие NaN в df:
   ```
   nans = df.isna().any().any()
   print(nans)
   ```
4) Отдыхаем, думаем что делать дальше

**Состав команды:**
* *Алексей*
* *Руслан*
* *Тигран*
