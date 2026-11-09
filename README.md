# STAT240-Final-Project

Group repository for our STAT 240 (Fall 2026) final project. This is the main place where we upload and share our files.

> **Status: draft framework only.** Nothing here is final. The topic, question, and method below are a starting point for discussion, and the topic must be agreed on by all group members.

## Initial topic idea: weather change in Madison

**Question of interest**

Is Madison's long-run mean January temperature different in 1995–2024 compared with 1965–1994?

"Long-run mean" means we are making an inference about the underlying climate in each period (a population parameter), not just describing the 30 Januaries we happen to observe.

**Data**
- Daily max/min temperatures from the NOAA weather station at Madison Dane County Regional Airport (station ID `USW00014837`), from NOAA's GHCN-Daily dataset. Records start in 1939 and are updated regularly.
- Download: https://www.ncei.noaa.gov/pub/data/ghcn/daily/by_station/USW00014837.csv.gz
- Format documentation: https://www.ncei.noaa.gov/pub/data/ghcn/daily/readme.txt
- Temperature values in the raw file are in tenths of a degree Celsius.

**Plan**
- Compute a daily mean temperature, (TMAX + TMIN) / 2, then average it over each January to get one value per year.
- This gives 30 values for each period. We use one value per year because temperatures on consecutive days are not independent.

**Method**
Inference on a difference of two means: a two-sample t-test (Welch), plus a 95% confidence interval for the difference.

**Planned graph**
Side-by-side boxplots of the January averages for the two periods.


