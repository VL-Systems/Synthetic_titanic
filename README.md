# Задача о выживании людей на синтетическом титанике 
На kaggle уже однажды проводилось соревнование да датасете с реальными пассажирами титаника вот ссылочка: https://www.kaggle.com/c/titanic
Это считается классической задачей которую должен попробывать начинающий DS специалист. 
Основной минус этой задачи был в том что находились люди, которые могли с первого раза определить кто выживет, а кто умрет из пассажиров и это выглядит как минимум странно.
Поэтому есть теория что такие люди просто нашли всю информацию о пассажирах и смогли воспользоваться её для решения задачи, что можно считать за 'читерство', но сложно доказуемо.
Видимо поэтому kaggle решил провести еще раз подобное соревнование идея так же самая, но вот все данные сгенерированны и их нельзя будет найти на сторонних источниках 
Ссылка на соревнование: https://www.kaggle.com/c/tabular-playground-series-apr-2021

### NaN
В данной задаче основной упор я делал на 'умную' замену пустных значений в датасете, то производить не простую замену на стационарное значение (например: fillna(median) или fillna(1)), а попытаться исследовать данные таким образом чтобы найти более сложные взаимосвязи и произвести 'умную' замену. 

### Ансамблирование моделей
Считается что использование 1 модели- проигрышная стратегия, поэтому лучше использовать месколько моделей. 
Это связано с тем, что каждая модель выделяет для себя наиболее важные признаки и не всегда у двух разных моделей будут одни и те же признаки иметь одинаковый вес. 
В коде после обучени так же проиводиться анализ призкаков и выделение наиболее ценных для конкретной модели
После улучшение каждой отдельной модели все модели ансамблируются и считается средний результат 

Решение можно скачать от сюда или перейти по ссылке и посмотреть на решение на kaggle: https://www.kaggle.com/lebedevav/tabular-playground-series-2
