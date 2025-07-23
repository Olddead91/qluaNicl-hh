# qlua
Quik Lua indicators

Всем привет. Здесь собраны индикаторы и скрипты, которые я написал для Квика.
Часть из них - это алгоритмы, реализованные в других торговых системах, другие - это проверка идей.

Важно:
Файлы на GitHub хранятся в кодировке UTF-8. Квик же понимает файлы только в кодировке win1251.
Поэтому, если вы просто скачиваете файл(ы), то необходимо обеспечить конвертацию в кодировку win1251.
Самой простой вариант - это сделать пустой файл в необходимо кодировке и вставить через буфер обмена текст.

Также обращаю внимание, что часть индикаторов и скриптов зависит от библиотек. Это видно по коду. Поэтому необходимо расположить необходимые библиотеки рядом запускаемым файлом.

Помогу с алгоритмизацией Ваших идей.

Мой блог
https://nick-nh.github.io

Для благодарностей: кошелек ЮMoney 410012258109375


## Список индикаторов

- [maLib.lua - Библиотека типовых методов сглаживания и вспомогательных функция для построения алгоритмов.](https://github.com/nick-nh/qlua/blob/master/maLib.lua)

    - Описание - https://nick-nh.github.io/2021-03-14/maLib
    - [MA.lua - Базовый пример использования библиотеки в индикаторе](https://github.com/nick-nh/qlua/blob/master/MA.lua)

- [k-mean.lua - k-means clustering.](https://github.com/nick-nh/qlua/blob/master/k-mean.lua)

   - https://ru.wikipedia.org/wiki/%D0%9C%D0%B5%D1%82%D0%BE%D0%B4_k-%D1%81%D1%80%D0%B5%D0%B4%D0%BD%D0%B8%D1%85

- [AMA.lua - Адаптивная скользящая средняя Перри Кауфмана.](https://github.com/nick-nh/qlua/blob/master/AMA.lua)

- [ATRNormalized.lua - Нормализованный ATR и побарный диапазон движения.](https://github.com/nick-nh/qlua/blob/master/ATRNormalized.lua)

- [AnchoredMomentum.lua - Smoothed Anchored Momentum by Rudy Stefenel.](https://github.com/nick-nh/qlua/blob/master/AnchoredMomentum.lua)

- [BidAskVol.lua - Побарная дельта объемов, собранная по обезличенным сделкам.](https://github.com/nick-nh/qlua/blob/master/BidAskVol.lua)

- [CenterOfGravity.lua - Center of Gravity Oscillator by John F. Ehlers.](https://github.com/nick-nh/qlua/blob/master/CenterOfGravity.lua)

  - https://www.mesasoftware.com/papers/TheCGOscillator.pdf

- [CyberCycle.lua - Adaptive version Cyber cycle by John F. Ehlers.](https://github.com/nick-nh/qlua/blob/master/CyberCycle.lua)

  - see his book `Cybernetic Analysis for Stocks and Futures`, Chapter 4: `Trading the Cycle`

- [DSMA.lua - Deviation-Scaled Moving Average by John F. Ehlers.](https://github.com/nick-nh/qlua/blob/master/DSMA.lua)

  - Featured in John F. Ehlers' article from July 2018 issue of Technical Analysis of Stocks & Commodities magazine, the DSMA (deviation-scaled moving average) is an adaptive moving average that rapidly adapts to volatility in price movement. It accomplishes this by modifying the alpha term of an EMA by the amplitude of an oscillator scaled in standard deviations from the mean. The DSMA's responsiveness can be changed by using different values for the input parameter period.

- [EFSDO.lua - Fisherized Deviation-Scaled Oscillator by John F. Ehlers.](https://github.com/nick-nh/qlua/blob/master/EFSDO.lua)

  - The FDSO (Fisherized Deviation-Scaled Oscillator) is featured in John F. Ehlers' article from October 2018 issue of Technical Analysis of Stocks & Commodities magazine. It's his DSO indicator with non-linear Fisher transform applied to it to make the oscillator suitable for swing trading through improving its probability distribution.

- [FisherTransform.lua - Fisher Transform by John F. Ehlers.](https://github.com/nick-nh/qlua/blob/master/FisherTransform.lua)

  - https://c.mql5.com/forextsd/forum/3/130fish.pdf

- [AutocorrelationPeriodogram.lua - Autocorrelation Periodogram by John F. Ehlers.](https://github.com/nick-nh/qlua/blob/master/AutocorrelationPeriodogram.lua)

  - https://traders.com/Documentation/FEEDbk_docs/2016/09/TradersTips.html

- [corrCycle.lua - Correlation angle by John F. Ehlers.](https://github.com/nick-nh/qlua/blob/master/corrCycle.lua)

  - https://www.mesasoftware.com/papers/CORRELATION%20AS%20A%20CYCLE%20INDICATOR.pdf

- [InstantaneousTrend.lua - Instantaneous trend by John F. Ehlers.](https://github.com/nick-nh/qlua/blob/master/InstantaneousTrend.lua)

  - https://c.mql5.com/forextsd/forum/59/023inst.pdf

- [MESA.lua - Adaptive Moving Averages by John F. Ehlers.](https://github.com/nick-nh/qlua/blob/master/MESA.lua)

  - The MESA Adaptive Moving Average ( MAMA ) adapts to price movement based on the rate of change of phase as measured by the Hilbert Transform Discriminator. This method features a fast attack average and a slow decay average so that composite average rapidly ratchets behind price changes and holds the average value until the next ratchet occurs. Consider FAMA (Following AMA) as the signal
  - https://mesasoftware.com/papers/MAMA.pdf


- [HeikenAshi.lua - Точки цвета баров HeikenAshi.](https://github.com/nick-nh/qlua/blob/master/HeikenAshi.lua)

  - т.к. терминал Квик не позволяет выводить бары на график, то выводятся точки цвета баров HeikenAshi поверх стандартных баров

- [Hurst.lua - Вычисление коэффициента Херста.](https://github.com/nick-nh/qlua/blob/master/Hurst.lua)

  - ресурсоемкий индикатор

- [MurreyLevels.lua - Уровни Мюррея.](https://github.com/nick-nh/qlua/blob/master/MurreyLevels.lua)

- [OnChartStochastic.lua - Осциллятор Стохастик выраженный в цене. Выводится поверх графика.](https://github.com/nick-nh/qlua/blob/master/OnChartStochastic.lua)

- [RenkoATR.lua - Реализация баров Ренко.](https://github.com/nick-nh/qlua/blob/master/RenkoATR.lua)

  - https://nick-nh.github.io/2021-01-17/renko

- [emaRenkoATR.lua - EMA поверх баров Ренко.](https://github.com/nick-nh/qlua/blob/master/emaRenkoATR.lua)

  - https://nick-nh.github.io/2021-01-17/renko

- [macdRenkoATR.lua - MACD поверх баров Ренко.](https://github.com/nick-nh/qlua/blob/master/macdRenkoATR.lua)

  - https://nick-nh.github.io/2021-01-17/renko

- [RegRenkoATR.lua - Регрессионный канал поверх баров Ренко.](https://github.com/nick-nh/qlua/blob/master/RegRenkoATR.lua)

- [SDSO.lua - Осциллятор Стохастик рассчитанный от стандартного отклонения.](https://github.com/nick-nh/qlua/blob/master/SDSO.lua)

- [StepNRTR.lua - Вариант индикатора Nick Rypock Trailing Reverse.](https://github.com/nick-nh/qlua/blob/master/StepNRTR.lua)

    - Основан на методике Константина Копыркина http://konkop.narod.ru/Files/4_24_28.pdf

- [_nrtr_myv 41.lua - Еще один вариант индикатора Nick Rypock Trailing Reverse.](https://github.com/nick-nh/qlua/blob/master/_nrtr_my%20v41.lua))

    - Динамический канал рассчитывается на основе ATR. Фильтрация скользящими средними.

- [TTM_Squeeze.lua - TTM Squeeze by John Carter.](https://github.com/nick-nh/qlua/blob/master/TTM_Squeeze.lua)

    - Bollinger Bands AND Keltner Channel define the market conditions, i.e. when BB is narrower than KC then we have a market squeeze. When BB break Outside the KC then trade in the direction of the smoothed Momentum.
    - https://school.stockcharts.com/doku.php?id=technical_indicators:ttm_squeeze

- [smTMMS.lua - TMMS - Trading Made More Simpler.](https://github.com/nick-nh/qlua/blob/master/smTMMS.lua)

    - The TMMS oscillator (aka “Trading Made More Simpler”) is an indicator made of conditions based on both 2 separated Stochastic and 1 RSI

- [JMA_Star_Light.lua - Jurik Research Jurik Moving Average.](https://github.com/nick-nh/qlua/blob/master/JMA_Star_Light.lua)

    - http://www.jurikres.com/catalog1/ms_ama.htm#top

- [JRSX.lua - Jurik Research Relative Strength Quality Index.](https://github.com/nick-nh/qlua/blob/master/JRSX.lua)

    - Jurik's RSX is a "noise free" version of RS
    - http://www.jurikres.com/catalog1/ms_rsx.htm

- [WaveTrend.lua - WaveTrend [LazyBear] vX by DGT.](https://github.com/nick-nh/qlua/blob/master/WaveTrend.lua)

    - https://ru.tradingview.com/script/cYG1lqRI-WaveTrend-LazyBear-vX-by-DGT/

- [barIndex.lua - Вывод индекса бара.](https://github.com/nick-nh/qlua/blob/master/barIndex.lua)

- [bigPeriodLines.lua - Индикатор вывода линий индикатора большего диапазона на меньший одного тикера.](https://github.com/nick-nh/qlua/blob/master/bigPeriodLines.lua)

  - Для примера, вывести с дневного графика на часовой и т.д.

- [dinapoli.lua - Уровни Джо ДиНаполи в виде гистограммы.](https://github.com/nick-nh/qlua/blob/master/dinapoli.lua)

- [dinapoliStoch.lua - Модификация стохастического осциллятора, описанная в книге Джо ДиНаполи.](https://github.com/nick-nh/qlua/blob/master/dinapoliStoch.lua)

- [EIS.lua - Elder Impulse System.](https://github.com/nick-nh/qlua/blob/master/EIS.lua)

- [extrLevels.lua - Поиск экстремумов движения цены.](https://github.com/nick-nh/qlua/blob/master/extrLevels.lua)

    - Если цена несколько раз достигает уровня на заданном периоде бар, при этом этот уровень не пробивался внутри периода.

- [fibo_ema.lua - EMA с выводом дополнительных канальных линий по уровням Фибоначчи.](https://github.com/nick-nh/qlua/blob/master/fibo_ema.lua)

- [fibo_ema_atr.lua - EMA с выводом дополнительных канальных линий по уровням Фибоначчи по ATR.](https://github.com/nick-nh/qlua/blob/master/fibo_ema_atr.lua)

    - Уровни откладываются от величины ATR. Дополнительно можно вывести TEMA, THV.

- [MA_ATR.lua - Скользящая средная с выводом канальных линий +/- ATR.](https://github.com/nick-nh/qlua/blob/master/MA_ATR.lua)

- [hourOpen.lua - Вывод уровня начала каждого часа.](https://github.com/nick-nh/qlua/blob/master/hourOpen.lua)

- [weekDayOpen.lua - Вывод уроня начала дня, недели.](https://github.com/nick-nh/qlua/blob/master/weekDayOpen.lua)

- [iReg.lua - Регрессия: линейная, параболическая, кубическая.](https://github.com/nick-nh/qlua/blob/master/iReg.lua)

- [kReg.lua - Nadaraya-Watson kernel regression.](https://github.com/nick-nh/qlua/blob/master/kReg.lua)

- [KalmanReg.lua - Kalman filter regression.](https://github.com/nick-nh/qlua/blob/master/KalmanReg.lua)

- [LSMA.lua - скользящее среднее наименьших квадратов.](https://github.com/nick-nh/qlua/blob/master/LSMA.lua)

- [AVDI.lua - Adaptive Volume-Demand-Index (AVDI).](https://github.com/nick-nh/qlua/blob/master/AVDI.lua)

- [lineFractals.lua - Вывод линий от найденных фрактальных уровней.](https://github.com/nick-nh/qlua/blob/master/lineFractals.lua)

- [pATR.lua - ATR, выраженный в процентах.](https://github.com/nick-nh/qlua/blob/master/pATR.lua)

- [priceAvgProfile.lua - Горизонтальные объемы, рассчитанные распределением объема по телу бара.](https://github.com/nick-nh/qlua/blob/master/priceAvgProfile.lua)

- [rangeFlatHV.lua - Сглаженная WVAP и поиск участков "флэт" методом линейной регрессии.](https://github.com/nick-nh/qlua/blob/master/rangeFlatHV.lua)

- [rangeHV.lua - Две сглаженные WVAP и уровень максимального интереса, найденный по горизонтальному профилю объемов.](https://github.com/nick-nh/qlua/blob/master/rangeFlatHV.lua)

- [regRangeBar.lua - Поиск участков "флэт" методом линейной регрессии.](https://github.com/nick-nh/qlua/blob/master/regRangeBar.lua)

- [autoLevels.lua - Поиск торговых диапазонов.](https://github.com/nick-nh/qlua/blob/master/autoLevels.lua)

- [tema.lua - TEMA - Triple Exponential Moving Average – Тройная Экспоненциальная Скользящая Средняя.](https://github.com/nick-nh/qlua/blob/master/tema.lua)

- [TMACD.lua - TEMA-EMA MACD как разница TEMA и EMA.](https://github.com/nick-nh/qlua/blob/master/TMACD.lua)

- [TEMABOL.lua - Bollinger bands от середнины TEMA и EMA.](https://github.com/nick-nh/qlua/blob/master/TEMABOL.lua)

- [thv_coral.lua - THV Coral- реализация Coral Trend Indicator.](https://github.com/nick-nh/qlua/blob/master/thv_coral.lua)

- [vsa.lua - Подсветка объемов по методике VSA.](https://github.com/nick-nh/qlua/blob/master/vsa.lua)

- [MarginCalc.lua - Расчет и вывод вариационной маржи (ГО) фьючерсного контракта для текущей цены.](https://github.com/nick-nh/qlua/blob/master/MarginCalc.lua)

- [vwap.lua - Вывод значения средневзвешенной цены из Таблицы текущих торгов (WAPRICE).](https://github.com/nick-nh/qlua/blob/master/vwap.lua)

- [min_max_price.lua - Вывод значений максимально и минимально возможной цены торговой сессии из Таблицы текущих торгов. Это позволит визуально оценивать допустимый диапазон цен установки лимитного ордера.](https://github.com/nick-nh/qlua/blob/master/min_max_price.lua)

- [smartZZ2 - Две версии индикатора Zig-Zag. Вывод целевых уровней движения цены. Определение паттернов.](https://github.com/nick-nh/qlua/blob/master/smartZZ2)

- [w32.dll - Сборка библиотеки w32.dll](https://github.com/nick-nh/qlua/blob/master/w32.dll.zip)

- [logging - Библиотека логгирования для qlua.](https://github.com/nick-nh/qlua/blob/master/logging)

    - Описание - https://nick-nh.github.io/2021-06-07/logLib

- [luaCOM - Сборка библиотеки luaCom.](https://github.com/nick-nh/qlua/blob/master/luaCOM)

    - Описание - https://nick-nh.github.io/2021-03-14/maLib

- [lua_socket_ssl - Сборка библиотек Socket, luaSec (SSL), lCurl.](https://github.com/nick-nh/qlua/blob/master/lua_socket_ssl)

- [quantScript - Скрипт сканирующий таблицу обезличенных сделок (ТОС)](https://github.com/nick-nh/qlua/blob/master/quantScript)

- [robot - Пример простого робота на qLua для терминала Квик](https://github.com/nick-nh/qlua/blob/master/robot)

- [tester - Пример простого тестера (оптимизатора) на qLua для терминала Квик](https://github.com/nick-nh/qlua/blob/master/tester)

- [scriptMonitor - Монитор (сканер) рынка для терминала Квик, для заданного списка тикеров](https://github.com/nick-nh/qlua/blob/master/scriptMonitor)

- [secScanner - Скрипт демонстратор: сканер рынка для терминала Квик, для заданного списка классов инструментов](https://github.com/nick-nh/qlua/blob/master/secScanner)

    - Описание - https://nick-nh.github.io/2021-06-20/secScanner-post

- [barsSaver - Скрипт выгружающий данные баров и алгоритмов, для заданного списка тикеров](https://github.com/nick-nh/qlua/blob/master/barsSaver)

    - Описание - https://nick-nh.github.io/2021-11-24/barsSaver-post

- [signalOrders - Скрипт, выполняющий команды, прочитанные из текстовых файлов, для заданного списка тикеров](https://github.com/nick-nh/qlua/blob/master/signalOrders)

    - Пример автоматизации - подписка на получение почтовых сообщений от сервиса TradingView по настроенным сигналам. Чтение почтового ящика, сохранение содержимого полученных писем в каталог, разбор их скриптом, выполнение команд. Т.о. автоматизируется выполнение торговых команд по сигналам TradingView. Также можно отправлять письма вручную, выполоняя свои команды.

- [telegramQuik - Решение для отправки (получения) сообщений из терминала Квик в Телеграм (telegram bot api), отправка почты](https://github.com/nick-nh/qlua/blob/master/telegramQuik)

    - https://nick-nh.github.io/2021-03-14/teleMessage

- [Сделки на графике из файлов формата Лучший частный инвестор](https://github.com/nick-nh/qlua/blob/master/invest_battle_pro)
