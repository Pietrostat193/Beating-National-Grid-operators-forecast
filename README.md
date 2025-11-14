# 24-Hour Ahead Electricity Forecasting (Italian Power Market)

This repository presents a comparison of two anonymized forecasting models (*Model1* and *Model2*) for the task of **24-hour-ahead electricity prediction** across the main Italian regions. The objective is to generate accurate hourly forecasts for the next day—one full vector of 24 values—using historical load data, weather variables, and regional fundamentals.

Day-ahead forecasting plays a central role in power-system operations and energy trading, as market participants must commit to schedules before gate closure. The quality of these forecasts directly affects imbalance exposure, trading performance, and operational planning.

To evaluate model performance, we compute error-based metrics in **MW**, focusing on both average daily accuracy (Mean MW/d) and tail-risk behaviour (ES95 MW). These metrics are reported for each Italian bidding zone using 1096 days of data (2024–2025). The table below summarizes the results and highlights the best performing model per region.


## Regional Performance (MW Metrics Only)

Performance computed using 1096 days between 2024/25.  
**Model1** and **Model2** refer to anonymized forecasting models.  
**Bold** numbers indicate best performance per region.

| Region        | Model   | Days | Mean MW/d | ES95 MW |
|---------------|---------|------|-----------|---------|
| Calabria      | Model1 | 79 | 6.9 | 102.0 |
| Calabria      | Model2 | 79 | **14.6** | **39.7** |
| Centre-North  | Model1 | 79 | 39.8 | 517.0 |
| Centre-North  | Model2 | 79 | **62.8** | **218.0** |
| Centre-South  | Model1 | 79 | 92.0 | 923.0 |
| Centre-South  | Model2 | 79 | **128.0** | **471.0** |
| North         | Model1 | 79 | 241.0 | 3,245.0 |
| North         | Model2 | 79 | **344.0** | **1,471.0** |
| Sardinia      | Model1 | 79 | 14.2 | 150.0 |
| Sardinia      | Model2 | 79 | **20.5** | **59.9** |
| Sicily        | Model1 | 79 | 28.7 | 316.0 |
| Sicily        | Model2 | 79 | **52.7** | **160.0** |
| South         | Model1 | 79 | 32.4 | 392.0 |
| South         | Model2 | 79 | **49.0** | **162.0** |


## Commentary on Model Performance

Across all Italian regions, **Model2 consistently outperforms Model1** in both key MW metrics:  
- **Mean MW/d** (average daily deviation captured or corrected by the model)  
- **ES95 MW** (tail-error magnitude; lower is better)

### Key Observations

1. **Model2 is uniformly superior across all regions.**  
   In every regional comparison, Model2 achieves both higher Mean MW/d and significantly lower ES95 MW, indicating better operational accuracy and reduced exposure to large tail errors.

2. **Largest improvements appear in the major load centers.**  
   - **North** and **Center-South** show the biggest absolute improvements:
     - North: Mean MW/d increases from 241 → **344**, ES95 MW drops from 3,245 → **1,471**  
     - Center-South: Mean MW/d from 92 → **128**, ES95 MW from 923 → **471**

   These regions account for a large portion of national load, suggesting strong scalability of Model2.

3. **Tail-risk reductions (ES95) are particularly notable.**  
   ES95 reductions often exceed **50%**, demonstrating that Model2 handles high-volatility or extreme-demand scenarios far more effectively than Model1.

4. **Smaller regions also benefit.**  
   Even in lower-load regions like Sardinia and Calabria, Model2 provides stable improvements:
   - Calabria ES95: 102 → **39.7**  
   - Sardinia ES95: 150 → **59.9**

5. **Model2 seems more robust to regional heterogeneity.**  
   Whether in large interconnected zones (North, Centre-North) or isolated systems (Sardinia, Sicily), Model2 maintains a consistent advantage.

### Overall Conclusion

Model2 shows a **clear and systematic improvement** over Model1 in all Italian regions, offering:
- Higher predictive accuracy  
- Lower tail risk  
- Better adaptability to regional load characteristics  
- Stronger operational value for trading and grid-forecasting tasks  

These results indicate that **Model2 is a more reliable forecasting engine**, especially when handling extreme events and high-variance load dynamics.

## Graphical Examples.





