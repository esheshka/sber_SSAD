# Репозиторий командной работы над проектом *Летней Школы Анализа Данных* от *ФКН* совместно со *Сбербанком*
## Капитан команды - **Юшинский Андрей Сергеевич**

**Мотивация:**
Одним из наиболее ценных источников информации о клиентах являются данные о банковских транзакциях. В этом наборе есть много ответов на вопрос: можно ли предсказать пол клиента, используя информацию о получении и оплате банковской картой? И если да, то какова точность такого прогноза?

**Задача:**
Cпрогнозировать AUC исходя из вероятности наличия пола (0/1) для каждого cid (идентификатора клиента), у которого отсутствует пол в файле gender.csv.

**Ограничение:**
Весь процесс обучения (от обработки данных до тренировки модели) должен укладываться в 2 минуты.

## Итог
**Точность модели: 88.487%**
**Занятое место: 3**

## Данные
**trx.csv** - таблица с хронологической историей транзакций за ~15 месяцев. В каждом cid может быть разное количество транзакций.
cid - идентификатор клиента банка; неотрицательное целое
число dt - дата транзакции; целое число, начинающееся с 0
mcc - mcc-код транзакции; целое число; внешний ключ для mcc в таблице _mcc.csv
ttc - тип транзакции; целое число; внешний ключ для ttc в таблице _ttc.csv
amt, сумма транзакций в некоторых денежных единицах, округленная до целого числа. Положительные/отрицательные значения - это зачисления/списания средств со счета клиента.
tid - идентификатор кассового терминала (торговой точки или POS-терминала), в котором была произведена транзакция.

**gender.csv** - таблица с числовым идентификатором cid и столбцами gender (0/1). Спрогнозируйте пол для строк, в которых отсутствует значение gender (т.е. первые несколько тысяч). Используйте оставшиеся значения gender в качестве целевых значений при обучении вашей модели.

**_mcc.csv** - таблица поиска с уникальными кодами торговых категорий (MCC) и их описаниями на русском языке. Это может быть полезно при поиске похожих категорий с использованием ключевых слов или семантики (например, с помощью векторов предложений).

**_ttc.csv** - справочная таблица с уникальными кодами типов транзакций и их словесным описанием на русском языке.
