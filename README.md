# Akatsuki [Pro+] · Expansion Model (4H)

A manual chart-reading indicator for TradingView, built to display custom 4-hour session candles and make session timing easier to read directly on the price chart.

This is a **visual charting tool**, not an automated trading system. It does not generate model signals or trade alerts. The goal is to give the trader a cleaner view of session candle structure so price action can be studied manually.

## Features

- **Projected 4H session candles** drawn alongside the main chart.
- **Session separators** to mark the start of each 4-hour session candle.
- **Time labels under separators**, anchored to the bottom of the chart pane.
- **Remaining-time label** for the active session in real time.
- Optional **HTF open line**.
- Optional **high and low lines** for completed session candles.
- Adjustable candle count, candle size, horizontal offset, body colors, border colors, and wick colors.
- Customizable HTF labels, interval labels, label positions, text colors, and text sizes.
- Configurable watermark text, position, color, size, and background.
- Separate session start times for non-FX and FX symbols, using New York local time.

## Session timing

The indicator uses `America/New_York` time.

Each session candle represents exactly four hours. The six session blocks run continuously throughout the day.

| **Session boundary** | **Non-FX symbols** | **FX symbols** |
| -------------------- | ------------------ | -------------- |
| ASIA 1             | 18:00              | 17:00          |
| ASIA 2             | 22:00              | 21:00          |
| LONDON             | 02:00              | 01:00          |
| NEW YORK AM 1             | 06:00              | 05:00          |
| NEW YORK AM 2            | 10:00              | 09:00          |
| NEW YORK PM             | 14:00              | 13:00          |

The FX schedule retains a one-hour offset from the non-FX schedule. Session times can be affected by New York daylight-saving changes because the script uses the New York time zone.

## Settings

### HTF Candles

Control whether projected candles are visible, how many candles are displayed, candle size, horizontal offset, bullish/bearish body colors, borders, and wicks. This section also contains the optional HTF Open trace, vertical separators, and high/low lines.

### Label Settings

Control the HTF label, remaining-time display, interval values, their colors and sizes, and where labels appear. The **Time Under Separators** option controls the session-time stamps shown at the bottom of the chart pane.

Separator-time text is displayed in Tiny size in this version.

### Watermark

Customize the watermark's visibility, position, brand text, color, size, and background.

## How to use

1. Open TradingView and open the **Pine Editor**.
2. Paste the indicator code into the editor and add it to the chart.
3. Use an intraday chart timeframe of **1 hour or lower** for the projected 4H session candles.
4. Customize the candle display, separators, labels, optional levels, and watermark in the indicator settings.
5. Read the session candle structure and surrounding price action manually.

## Important notes

- The projected session candles are assembled from the active chart's bars; they are not native exchange-provided 4-hour candles. The chart timeframe can affect the granularity of the session aggregation, especially around session boundaries.
- The active-session remaining-time display is intended for realtime use; historical bars do not provide a live countdown.
- The 4H projection is restricted to 1H and lower chart timeframes.
- This version intentionally excludes the 4H Profile Expansion dashboard, sweep displays, EQ/midpoint lines, CISD/IC-CISD, automated setup detection, and trade alerts.
- Review the script in Pine Editor and test the display on your preferred symbols and timeframes before relying on it.

## Disclaimer

This indicator is for chart visualization and educational study only. It is not financial advice and does not promise trading results. Trading involves risk; make independent decisions and manage risk appropriately.
