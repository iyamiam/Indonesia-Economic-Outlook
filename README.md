# Indonesia-Economic-Outlook
Libraries & Tools Used:

Tools:
Visual Studio Code
Python
Jupyter Notebook

Libraries:
Pandas
Statsmodels

Models:
ARIMA (Autoregressive Integrated Moving Average)
Used for forecasting and filling the missing years 2024 & 2025
ETS (Exponential Smoothing / Holt Method)
Used for forecasting 2026 & 2027

The main data is taken from :

IMF APD Regional Economic Outlook

Period: 2000–2023
Indikator:
GDP constant prices (% change)
CPI (end-of-period & period average)
Current account balance (% of GDP)
Net lending/borrowing (% of GDP)
Unemployment rate
GDP PPP per capita (% change)

Data tambahan 2024–2025 dari BPS

1. Inflasi (CPI) – BPS 2024–2025

Source: Badan Pusat Statistik (BPS)

CPI 2024 → 1.57% (realese BPS Descember 2024)

CPI 2025 → 2.72% YoY (rilis BPS November 2025)

2. (Unemployment Rate) – BPS 2024–2025

Source: BPS Tingkat Pengangguran Terbuka (TPT)

TPT 2024 → 4.91% (Agustus 2024)

TPT 2025 → 4.85% (Agustus 2025)

3.Economic Growth (GDP Growth) – Quarterly Data from BPS

Since the annual figure for 2025 is not yet available, only the following are available:

Q1-2025: 4.87% YoY

Q2-2025: 5.12% YoY

Q3-2025: 5.04% YoY

Since the complete annual data is not yet available, the 2025 GDP indicator is still forecasted using ARIMA.

4. Other indicators (Current Account, Net Lending, GDP PPP per capita)

There are no complete and annual official publications for 2024–2025.

These indicators are still forecasted using ARIMA.

Forecasting Methodology:
a. Filling in 2024 (ARIMA)
For indicators that do not have 2024 data in the IMF
Predicted using ARIMA(1,1,1) with input data from 2000–2023

Indicators that already have 2024 data left as is.

b. Filling in 2025

If actual BPS data is available (e.g., CPI and unemployment rate), it will be used.

If not, ARIMA(1,1,1) is used to predict 2025 using data from 2000–2024.

c. Forecast for 2026–2030 (ETS)

After data for 2000–2025 is complete (actual + ARIMA),
the next five years are forecasted using:
Exponential Smoothing with additive trend

Reasons for using ETS:
Annual data has no seasonality
ETS is more stable than ARIMA for multi-step (more than one year) forecasting

Forecast Conclusions by Indicator:

1.Net Lending / Borrowing (Government Fiscal Position)
Mild but stable deficit; not worsening, gradually improving.

2.GDP Growth (Economic Growth)
3.3–4.3%, moderate and consistent growth.

3.Current Account Balance
Mild deficit –0.14 to –1.07%, stable and well-controlled

4.CPI (End-of-Period)
1.0–2.7%, low and stable inflation.

5.CPI (Period Average)
1.0–2.5%, follows the EoP inflation pattern, remains controlled.

6.Unemployment Rate
4.6–4.8%, stable with no risk of a spike in unemployment.

7.GDP PPP per Capita Growth
Moderate upward trend, purchasing power increases gradually.
