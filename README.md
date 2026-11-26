# Kazakhstan precipitation outlook during the 2026 El Niño

Experimental, non-operational seasonal precipitation outlook for Kazakhstan
for winter (DJF 2026-27) and spring (MAM 2027), issued during the strong
2026 El Niño. The outlook was fixed **before** the observation of the
forecast seasons; it will be verified against ERA5 in 2027.

**Version:** v1.0  
**Issued:** 2026-11-26  
**Author:** Sanimgul Nazarbekova

## Contents

- `outlook/`: the outlook document (PDF) with forecast table, method, caveats and verification criteria
- `notebooks/`: Google Colab notebook that reproduces all results

## Method (short)

1. ERA5 monthly total precipitation (1950-2025), cropped to Kazakhstan.
2. Seasonal sums (OND, DJF, MAM, JJA) and a 1991-2020 climatology.
3. Four zones within Kazakhstan's borders: all country, north (>50°N),
   centre (45-50°N), south (<45°N).
4. Analysis of strong El Niño events (ONI >= 2.0, 1979 onwards: 1982-83,
   1997-98, 2015-16) and correlation/regression of seasonal precipitation
   on the Oceanic Niño Index (ONI).
5. Scenario-based outlook (ONI = 2.0, 2.5, 3.0) with 80% prediction intervals.

## Limitations

- The ONI explains only about 10-20% of interannual precipitation variance.
- The 2026 event may exceed the historical range, so the regression extrapolates.
- Probabilities are model outputs on a small sample and are likely overconfident.
- ERA5 precipitation is model-derived and less reliable in mountain areas.
- NAO, Arctic Oscillation and the Indian Ocean Dipole are not included.

## Verification (planned)

After the seasons end, observed ERA5 anomalies will be compared with the
outlook using criteria fixed in advance (sign and 80% interval). All results,
including failures, will be reported in this repository.

## Data

- ERA5 reanalysis: Hersbach et al., Copernicus Climate Change Service (C3S)
  Climate Data Store. Not redistributed here; the notebook shows how to download it.
- ONI: NOAA Climate Prediction Center.

## License

Code: MIT.
