# Multi-Indicator System [15M-30M-1H]

This Pine Script is designed to provide a comprehensive trading system that integrates multiple technical indicators across different timeframes (15 minutes, 30 minutes, and 1 hour). The script includes Ichimoku Cloud, RSI, MACD, SMA, and EMA indicators, each of which can be customized based on the selected timeframe. Additionally, it incorporates a weighted scoring system to generate a final trading signal.

## Features

- **Timeframe Adaptation**: Automatically adjusts parameters for Ichimoku, RSI, MACD, SMA, and EMA based on the selected timeframe (15M, 30M, or 1H).
- **Ichimoku Cloud**: Displays Senkou A and Senkou B lines with customizable lengths and displacement.
- **RSI**: Calculates Relative Strength Index with adjustable length and overbought/oversold levels.
- **MACD**: Computes Moving Average Convergence Divergence with customizable fast, slow, and signal line periods.
- **Moving Averages**: Includes Simple Moving Average (SMA) and Exponential Moving Average (EMA) with adjustable lengths.
- **Weighted Scoring System**: Assigns weights to each indicator to calculate a final trading signal.
- **Compact Table**: Displays real-time signals from each indicator in a compact table format on the chart.
- **Background Color**: Changes the background color based on the price's position relative to the Ichimoku cloud.

## Usage

1. **Install Pine Script**: Copy the script into your TradingView Pine Editor.
2. **Select Timeframe**: The script automatically detects the current timeframe and adjusts the indicator parameters accordingly.
3. **Customize Parameters**: Modify the input parameters to suit your trading strategy.
4. **Analyze Signals**: Use the compact table and background color to interpret the overall market sentiment.

## Input Parameters

### Timeframe Detection
- `is_15m`: Detects if the current timeframe is 15 minutes.
- `is_30m`: Detects if the current timeframe is 30 minutes.
- `is_1h`: Detects if the current timeframe is 1 hour.

### Ichimoku Parameters
- `tenkan_len_15m`, `tenkan_len_30m`, `tenkan_len_1h`: Length of the Tenkan-sen line for 15M, 30M, and 1H timeframes.
- `kijun_len_15m`, `kijun_len_30m`, `kijun_len_1h`: Length of the Kijun-sen line for 15M, 30M, and 1H timeframes.
- `senkou_b_len_15m`, `senkou_b_len_30m`, `senkou_b_len_1h`: Length of the Senkou Span B line for 15M, 30M, and 1H timeframes.
- `displacement`: Displacement value for the future projection of Senkou Span A and B.

### RSI Parameters
- `rsi_length_15m`, `rsi_length_30m`, `rsi_length_1h`: Length of the RSI calculation for 15M, 30M, and 1H timeframes.
- `rsi_overbought`, `rsi_oversold`: Overbought and oversold levels for RSI.

### MACD Parameters
- `macd_fast_15m`, `macd_fast_30m`, `macd_fast_1h`: Fast period for MACD calculation for 15M, 30M, and 1H timeframes.
- `macd_slow_15m`, `macd_slow_30m`, `macd_slow_1h`: Slow period for MACD calculation for 15M, 30M, and 1H timeframes.
- `macd_signal_15m`, `macd_signal_30m`, `macd_signal_1h`: Signal line period for MACD calculation for 15M, 30M, and 1H timeframes.

### Moving Averages Parameters
- `sma_length_15m`, `sma_length_30m`, `sma_length_1h`: Length of the SMA for 15M, 30M, and 1H timeframes.
- `ema_length_15m`, `ema_length_30m`, `ema_length_1h`: Length of the EMA for 15M, 30M, and 1H timeframes.

### Weighted Scoring System
- `weights`: Array of weights assigned to each indicator (Ichimoku, RSI, MACD, SMA, EMA).

## Logic and Visualization

- **Ichimoku Cloud**: Calculates and plots Senkou A and Senkou B lines. Background color changes based on the price's position relative to the cloud.
- **RSI**: Calculates and normalizes the RSI value.
- **MACD**: Calculates and normalizes the MACD line relative to its signal line.
- **Moving Averages**: Plots SMA and EMA lines on the chart.
- **Final Signal**: Combines the normalized values of all indicators using the weighted scoring system to generate a final trading signal displayed in the compact table.

## Example Usage

To use this script, simply copy and paste it into the Pine Editor on TradingView. Adjust the input parameters as needed, and apply the script to your desired chart. The compact table will display real-time signals from each indicator, and the background color will help you quickly assess the market sentiment.

## Disclaimer

This script is provided for educational purposes only. It is not intended to be used as financial advice. Always conduct thorough research and backtest any trading strategy before applying it to live markets. 

---- 

Этот скрипт Pine Script предназначен для предоставления комплексной торговой системы, которая интегрирует несколько технических индикаторов на разных таймфреймах (15 минут, 30 минут и 1 час). Скрипт включает Ишимоку Клауд, RSI, MACD, SMA и EMA индикаторы, каждый из которых можно настроить в зависимости от выбранного таймфрейма. Кроме того, он включает взвешенную систему оценки для генерации финального торгового сигнала.

## Особенности

- **Адаптация под таймфрейм**: Автоматически регулирует параметры для Ишимоку, RSI, MACD, SMA и EMA в зависимости от выбранного таймфрейма (15М, 30М или 1Ч).
- **Ишимоку Клауд**: Отображает линии Сенко А и Сенко В с настраиваемыми длинами и смещением.
- **RSI**: Вычисляет Индекс относительной силы с настраиваемой длиной и уровнями перекупленности/перепроданности.
- **MACD**: Вычисляет Схождение-расхождение скользящих средних с настраиваемыми периодами быстрой, медленной и сигнальной линий.
- **Скользящие средние**: Включает Простую скользящую среднюю (SMA) и Экспоненциальную скользящую среднюю (EMA) с настраиваемыми длинами.
- **Взвешенная система оценки**: Назначает веса каждому индикатору для расчета финального торгового сигнала.
- **Компактная таблица**: Отображает сигналы в реальном времени от каждого индикатора в компактной таблице на графике.
- **Цвет фона**: Меняет цвет фона в зависимости от положения цены относительно облака Ишимоку.

## Использование

1. **Установка Pine Script**: Скопируйте скрипт в ваш редактор Pine Script на TradingView.
2. **Выбор таймфрейма**: Скрипт автоматически определяет текущий таймфрейм и регулирует параметры индикаторов соответственно.
3. **Настройка параметров**: Измените входные параметры в соответствии с вашей торговой стратегией.
4. **Анализ сигналов**: Используйте компактную таблицу и цвет фона для интерпретации общего рыночного настроения.

## Входные параметры

### Определение таймфрейма
- `is_15m`: Определяет, если текущий таймфрейм составляет 15 минут.
- `is_30m`: Определяет, если текущий таймфрейм составляет 30 минут.
- `is_1h`: Определяет, если текущий таймфрейм составляет 1 час.

### Параметры Ишимоку
- `tenkan_len_15m`, `tenkan_len_30m`, `tenkan_len_1h`: Длина линии Тенкан-сен для таймфреймов 15М, 30М и 1Ч.
- `kijun_len_15m`, `kijun_len_30m`, `kijun_len_1h`: Длина линии Кижун-сен для таймфреймов 15М, 30М и 1Ч.
- `senkou_b_len_15m`, `senkou_b_len_30m`, `senkou_b_len_1h`: Длина линии Сенко Спан Б для таймфреймов 15М, 30М и 1Ч.
- `displacement`: Значение смещения для будущего проектирования линий Сенко Спан А и В.

### Параметры RSI
- `rsi_length_15m`, `rsi_length_30m`, `rsi_length_1h`: Длина вычисления RSI для таймфреймов 15М, 30М и 1Ч.
- `rsi_overbought`, `rsi_oversold`: Уровни перекупленности и перепроданности для RSI.

### Параметры MACD
- `macd_fast_15m`, `macd_fast_30m`, `macd_fast_1h`: Быстрый период для вычисления MACD для таймфреймов 15М, 30М и 1Ч.
- `macd_slow_15m`, `macd_slow_30m`, `macd_slow_1h`: Медленный период для вычисления MACD для таймфреймов 15М, 30М и 1Ч.
- `macd_signal_15m`, `macd_signal_30m`, `macd_signal_1h`: Период сигнальной линии для вычисления MACD для таймфреймов 15М, 30М и 1Ч.

### Параметры скользящих средних
- `sma_length_15m`, `sma_length_30m`, `sma_length_1h`: Длина SMA для таймфреймов 15М, 30М и 1Ч.
- `ema_length_15m`, `ema_length_30m`, `ema_length_1h`: Длина EMA для таймфреймов 15М, 30М и 1Ч.

### Взвешенная система оценки
- `weights`: Массив весов, назначенных каждому индикатору (Ишимоку, RSI, MACD, SMA, EMA).

## Логика и визуализация

- **Ишимоку Клауд**: Вычисляет и отображает линии Сенко А и Сенко В. Цвет фона изменяется в зависимости от положения цены относительно облака.
- **RSI**: Вычисляет и нормализует значение RSI.
- **MACD**: Вычисляет и нормализует линию MACD относительно сигнальной линии.
- **Скользящие средние**: Отображает линии SMA и EMA на графике.
- **Финальный сигнал**: Объединяет нормализованные значения всех индикаторов с использованием взвешенной системы оценки для генерации финального торгового сигнала, отображаемого в компактной таблице.

## Пример использования

Для использования этого скрипта просто скопируйте и вставьте его в редактор Pine на TradingView. Настройте входные параметры по мере необходимости и примените скрипт к вашему графику. Компактная таблица будет отображать сигналы в реальном времени от каждого индикатора, а цвет фона поможет вам быстро оценить рыночное настроение.

## Отказ от ответственности

Этот скрипт предоставляется исключительно в образовательных целях. Он не предназначен для использования в качестве финансового совета. Всегда проводите тщательное исследование и тестирование любой торговой стратегии перед её применением на живых рынках.

---

Не стесняйтесь форкать этот проект, вносить улучшения и делиться своими улучшениями с сообществом!

---

Feel free to fork this project, make improvements, and share your enhancements with the community!
