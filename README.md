# Aviation Accident Analysis

## Overview

This project analyzes aviation accident data to identify aircraft manufacturers and models associated with lower rates of aircraft destruction and serious or fatal passenger injuries.

The analysis focuses on professionally built airplanes from 1983 onward and separates smaller and larger aircraft using a threshold of 20 people.

## Business Problem

An aviation insurance company is interested in understanding which aircraft makes and models have historically experienced less severe outcomes when accidents occur.

The analysis focuses on:

- Serious and fatal passenger injury rates
- Aircraft destruction rates
- Differences between smaller and larger aircraft
- Differences between aircraft manufacturers and specific models
- Other factors associated with accident severity

## Data

The project uses aviation accident data covering aircraft accidents and their outcomes.

The data was cleaned by:

- Converting event dates to datetime values
- Limiting the analysis to professionally built airplanes
- Limiting accidents to 1983 and later
- Standardizing aircraft manufacturer names
- Removing aircraft models with missing model information
- Creating a serious/fatal injury rate
- Creating a binary aircraft destruction indicator
- Cleaning missing and unknown categorical values

## Analysis

Aircraft were separated into:

- **Smaller aircraft:** fewer than 20 people
- **Larger aircraft:** 20 or more people

Safety was evaluated using:

1. Mean serious/fatal injury rate
2. Aircraft destruction rate

Aircraft makes and specific plane types were compared separately. Plane-type comparisons required at least 10 observations to reduce the influence of very small samples.

The project also examined two additional factors:

- **Weather Condition**
- **Phase of Flight**

## Key Findings and Recommendations
### Aircraft Makes

For smaller aircraft, Grumman Acft Eng Cor-Schweizer, Stinson, Aviat Aircraft Inc., Maule, and DeHavilland showed relatively favorable results when considering both serious/fatal injury rates and aircraft destruction rates.

For larger aircraft, McDonnell Douglas, Bombardier, Boeing, and Embraer generally showed relatively low serious/fatal injury and destruction rates among the recorded accidents.

### Aircraft Models

Safety outcomes varied between specific aircraft models even when they were produced by the same manufacturer. Model-level comparisons were therefore limited to aircraft types with at least 10 observations to reduce the influence of very small samples.

### Weather

Weather condition was strongly associated with accident severity. Accidents occurring in instrument meteorological conditions (IMC) had higher serious/fatal injury rates and destruction rates than accidents occurring in visual meteorological conditions (VMC).

### Phase of Flight

Accident severity also varied by phase of flight. Landing accidents were relatively common but had comparatively low serious/fatal injury and destruction rates. Other phases, including climbing and maneuvering, showed more severe outcomes.

### Recommendation

For an insurer evaluating aircraft risk, both manufacturer and specific aircraft model should be considered rather than relying on manufacturer alone. Weather conditions and phase of flight should also be considered because both were associated with substantial differences in accident severity.

## Important Limitation

This dataset contains accident records rather than total aircraft operations. Therefore, the results describe the severity of recorded accidents and should not be interpreted as the overall probability that a particular aircraft will experience an accident.

Exposure measures such as total flights, flight hours, and fleet size would be needed to estimate overall accident risk.

## Repository Structure

- `Aviation_Accidents_Cleaning.ipynb` — data cleaning and preparation
- `Aviation_Accidents_Data_Analysis.ipynb` — exploratory analysis, visualizations, and recommendations
- `data/AviationData_Clean.csv` — cleaned dataset used for analysis
- `README.md` — project overview and findings

## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
