# Практическая работа №1. Анализ данных мониторинга и моделирования для городов

### Часть 1 
* Исследовать доступность данных станционных наблюдений для выбранного города и его окрестностей (метеостанции, аэропорты, специализированные сети)
* Выбрать репрезентативные городские и загородные станции 
  + Если таких станций нет - выбрать другой город
* Определить точное местоположение этих станций
* Скачать данные за несколько лет
* Построить графики временной динамики основных метеовеличин (температуры, влажности, скорости ветра) ветра на городских и загородных станциях за месяцы с контрастными метеоусловиями, например, для лета/зимы (см. пример в [PW1_example1](https://github.com/mvarentsov/Urban-climate-modelling4HSE/blob/main/Practice/PW1_example1.ipynb))
* Проанализировать городские аномалии температуры и влажности(разности «город-фон») (см. пример в [PW1_pandas_demo](https://github.com/mvarentsov/Urban-climate-modelling4HSE/blob/main/Practice/PW1_pandas_demo.ipynb))
  + Построить графики временной динамики за отдельные периоды (≈15-30 дней)
  + Построить график осредненного суточного хода 
  + Построить график осредненного сезонного хода

### Часть 2
* Добавить в список анализируемых метеостанций хотя бы еще одну фоновую или городскую станцию (чтобы хотя бы одна выборка включала не менее двух станций)
* При решении заданий из части 1 использовать средние  значения по выборке городских/фоновых станций (см. пример в [PW1_pandas_demo](https://github.com/mvarentsov/Urban-climate-modelling4HSE/blob/main/Practice/PW1_pandas_demo.ipynb))
* Рассчитать по данным наблюдений на загородных станциях эмпирический «фактор погоды» ([Oke, Runnalls, 2000](https://www.tandfonline.com/doi/abs/10.1080/02723646.2000.10642711), [Varentsov et al. 2023](https://www.mdpi.com/2225-1154/11/10/200))
  ![image](https://github.com/mvarentsov/Urban-climate-modelling4HSE/assets/67764064/e64a2bdd-d975-4e75-98d1-7c4c72de3727)
* Исследовать статистическую связь между «фактором погоды» и разностью температуры «город-фон» (рассчитать коэффициент корреляции, построить "диаграмму рассеяния")
  
### Часть 3 
* Скачать данные реанализа ERA5 для выбранного города и его окрестностей в [Copernicus Data Store](https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-single-levels?tab=overview):
  + нужны приземные переменные, включая все те, что на скриншоте Panoply Data Viewer (они нам еще пригодятся)
  ![image](https://github.com/mvarentsov/Urban-climate-modelling4HSE/assets/67764064/d6139656-e55a-4c0e-af58-77a54f77168b)
  + за тот же период, что и анализируемые наблюдения
* Построить карты средних значений температуры и скорости ветра для двух контрастных сезонов (см. пример в [PW1_example_ERA5](https://github.com/mvarentsov/Urban-climate-modelling4HSE/blob/main/Practice/PW1_example_ERA5.ipynb))
* Интерполировать данные реанализа в точки расположения метеостанций (см. пример в [PW1_example_ERA5](https://github.com/mvarentsov/Urban-climate-modelling4HSE/blob/main/Practice/PW1_example_ERA5.ipynb))
* Построить графики динамики температуры и скорости ветра по данным реанализа и наблюдений
* Построить графики суточного хода средних (ME) и среднеквадратичных (RMSE) ошибок реанализа для городской и фоновой станций

