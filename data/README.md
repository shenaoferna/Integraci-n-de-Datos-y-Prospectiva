# Data

> **Synthetic data.** Both datasets were generated with AI for a university course. AndesMed and Glacia Health Logistics are fictional companies.

| File | What it is |
|---|---|
| `DF_AndesMed_Cold_Chain_LDA_v2.csv` | Internal data: 1,500 days of operation of AndesMed |
| `DF_Glacia_Health_external_data_v2.xlsx` | External data: 1,500 days of operation of Glacia Health Logistics |
| `DF_Integrated_AndesMed_Glacia_1000.csv` | Output: the integrated 1,000-record dataset (created by the notebook, with English column names and values) |

Each row is **one day of operation**. The two source files keep their original Spanish column names and values; the notebook translates them when it loads the data:

| Column in the notebook (original name) | Description |
|---|---|
| `ID` | Record number (repeats across both files) |
| `Date` (`Fecha`) | Date (2022-01-01 to 2026-02-08) |
| `Vehicle_Type` (`Tipo_Vehiculo`) | Main vehicle that day: refrigerated truck, refrigerated van or small refrigerated van |
| `Route` (`Ruta`) | Main route that day (6 national routes) |
| `Main_Cause` (`Causa_Principal`) | Main cause of that day's cold-chain breaks |
| `Break_Frequency` (`Frecuencia_Ruptura`) | Number of cold-chain breaks that day |
| `Severity_COP` (`Severidad_COP`) | Average cost per break (COP) |
| `LDA` | Daily loss = frequency × severity (COP) |
| `Shipments` (`Envios`) | Number of refrigerated shipments that day |
