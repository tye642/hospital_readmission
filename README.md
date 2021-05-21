# hospital-readmission-analysis
Analysis of hospital readmission data with Ursa Health

## Questions

1. What is our 30-day all cause readmission rate across hospitals our members are admitted to?
2. What percent of patients have a PCP visit within a week of discharge?
3. Do either vary by individual or group PCP's?

#### Bonus: 

4. Which individual or PCP groups should we make an extra effort with to build a relationship? Which have the highest volume?
5. What percent of our patients do not have a PCP assigned or haven't seen their PCP recently?
6. Are there certain patients we should focus on (e.g. frequent fliers)?
7. From this, what could a version 1 of an actionable dashboard or intervention list look like to support the Transition Care Managers?

## Data

- **Membership**: One row per patient-plan-period during which the patient was an active member of the health plan
- **Inpatient Admissions**: One record per hospital inpatient admission encounter; this object executes the logic to generate the final encounter-level properties based on the full set of documents related to the encounter collected in the aggregator object.
- **Primary Care Provider Office Visits**: One record per office visit with a primary care clinician, or in which primary care services were delivered; clinician office visits meeting any of the following criteria are considered primary care:
    -  A service provider or attending provider with a qualifying primary care primary specialty
    -  A HCPS code associated with preventive primary care services
    -  A service provider, attending provider, or provider group provider designated as a primary care provider in the Providers object
