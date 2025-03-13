# Open SDG - Test site

## Index of tests

### 1. Series/Unit/Disaggregation selection
##### 1.1.1 Series
##### 1.1.2 Unit
##### 1.1.3 Single disaggregation selection
##### 1.2.1 Multiple series selection
##### 1.2.2 Multiple unit selection
##### 1.2.3 Multiple disaggregation selection
##### 1.3.1 Series/Unit selection
##### 1.3.2 Series/disaggregation selection
##### 1.3.3 Unit/disaggregation selection
##### 1.3.4 Series, unit, and disaggregation selection
##### 1.4.1 Selection not sufficiently reduced by user --> Error during build
##### 1.4.2 Error in series/unit/disaggregation selection --> Warning if can be ignored, Error if critical
##### 1.4.3 Empty data file --> Warn user and set not_available
##### 1.4.4 No data file --> Warn user and set not_available

### 2. Progress column
##### 2.1.1 Progress column with valid data
##### 2.1.2 Progress column with invalid data --> Warn user and set not_available
##### 2.1.3 Empty progress column --> Warn user, no data found
##### 2.2.1 Progress column with series selection
##### 2.2.2 Progress column with unit selection
##### 2.2.3 Progress column with disaggregation selection
##### 2.2.4 Progress column with selection insufficiently reduced by user --> Error during build

### 3. Limits
##### 3.1.1 Qualitative indicator with maximum limit
##### 3.1.2 Qualitative indicator with minimum limit
##### 3.1.3 Qualitative indicator with limit, but wrong direction --> Warn user
##### 3.1.4 Qualitative indicator with limit, base value = limit
##### 3.2.1 Quantitative indicator with limit --> Warn user and ignore the limit

### 4. General
##### 4.1.1 Qualitative, all positive values, positive direction
##### 4.1.2 Qualitative, all positive values, negative direction
##### 4.2.1 Quantitative, all positive values, positive direction
##### 4.2.2 Quantitative, all positive values, negative direction
##### 4.3.1 Quantitative, all positive values, positive direction, target achieved at t = 0
##### 4.3.2 Quantitative, all positive values, negative direction, target achieved at t = 0
##### 4.4.1 Qualitative, all negative values, positive direction
##### 4.4.2 Qualitative, all negative values, negative direction
##### 4.5.1 Quantitative, all negative values, positive direction
##### 4.5.2 Quantitative, all negative values, negative direction
##### 4.6.1 Quantitative, all negative values, positive direction target achieved at t = 0
##### 4.6.2 Quantitative, all negative values, negative direction, target achieved at t = 0
##### 4.7.1 Mix of positive and negative values --> Warn user and set not_available
##### 4.8.1 Manual override --> score = None, progress_status = whatever the user provided
##### 4.9.1 Not enough data points --> Warn user and set not_available

### 5. Zeros
##### 5.1.1 Target = 0 --> Warn user and set target = 0.001
##### 5.2.1 Base_value = 0 --> Warn user and set base value = 0.001
##### 5.3.1 Current_value = 0 --> progress_value = +/-1
##### 5.4.1 Limit = 0 --> base_value >= 2*limit so coeff = 1 and limit is effectively ignored

### 6. Score
##### 6.1.1 Qualitative indicator with CAGR = 2%, score should be 5
##### 6.1.2 Qualitative indicator with CAGR = 1.5%, score should be 2.5
##### 6.1.3 Qualitative indicator with CAGR = 0.5%, score should be 0
##### 6.1.4 Qualitative indicator with CAGR = 0%, score should be -2.5
##### 6.1.5 Qualitative indicator with CAGR = -1%, score should be -3.75
##### 6.1.6 Qualitative indicator with CAGR = -2%, score should be -5
##### 6.2.1 Qualitative indicator near limit with CAGR/coeff = 2%, score should be 5
##### 6.2.2 Qualitative indicator near limit with CAGR/coeff = 1.5%, score should be 2.5
##### 6.2.3 Qualitative indicator near limit with CAGR/coeff = 0.5%, score should be 0
##### 6.2.4 Qualitative indicator near limit with CAGR/coeff = 0%, score should be -2.5
##### 6.2.5 Qualitative indicator near limit with CAGR = -1%, score should be -3.75
##### 6.2.6 Qualitative indicator near limit with CAGR = -2%, schore should be -5
##### 6.3.1 Quantitative indicator, multiple disaggregations, limited progress, no target achieved 
##### 6.3.2 Quantitative indicator, multiple disaggregations, limited progress, some targets achieved
##### 6.3.3 Quantitative indicator, multiple disaggregations, limited progress, all targets achieved --> (5, target_achieved)
##### 6.3.4 Quantitative indicator, multiple disaggregations, substantial progress (scores=[5,5,5,5]), no targets achieved --> (5, substantial_progress)
##### 6.3.5 Quantitative indicator, multiple disaggregations, substantial progress (scores=[5,5,5,5]), some targets achieved --> (5, substantial_progress)
##### 6.3.6 Quantitative indicator, multiple disaggregations, substantial progress (scores=[5,5,5,5]), all targets achieved --> (5, target_achieved)

### 7. Other
##### 7.1.1 Data start values after changing series
##### 7.2.1 Observation attributes and GeoCode
##### 7.3.1 No progress status, manual override
##### 7.3.2 Non-statistical indicator, manual override
