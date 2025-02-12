---
title: "How Do Polycentric Urban Structures Affect Household Carbon Emissions? Evidence from Household Surveys"
excerpt: "Against the backdrop of global climate change, how urban spatial structures shape low-carbon lifestyles has become a key issue. A recent study published in the journal 'Cities'—'The role of polycentric urban structures in shaping low-carbon lifestyles'—draws on Chinese household energy consumption data to reveal the mechanisms and urban–rural differences in how polycentric urban development affects household carbon emissions, providing important insights for sustainable urban planning.<br/><img src='/images/p6.jpg'>"
date: 2025-2-11
collection: portfolio
---

### Introduction

Against the backdrop of global climate change, how urban spatial structures shape low-carbon lifestyles has become a key issue. A recent study published in the journal "Cities," titled "The Role of Polycentric Urban Structures in Shaping Low-Carbon Lifestyles," draws on Chinese household energy consumption data to reveal how the development of polycentric cities affects household carbon emissions, shedding light on its impact mechanisms and urban–rural differences. This provides important insights for sustainable urban planning.

---

## 1. Research Background: How Does Urban Structure Drive Carbon Emissions?

The household sector is a major source of carbon emissions, accounting for more than 30% of China’s total carbon emissions. Traditional research has focused on whether monocentric or polycentric city structures are better, but the findings remain inconclusive:  
- Monocentric (economic activities concentrated in the CBD) may exacerbate traffic congestion and pollution.  
- Polycentric (multiple sub-centers in a dispersed layout) may shorten commuting distances, yet potentially increase energy consumption due to higher incomes and larger housing areas.

China is undergoing rapid urbanization, and polycentric structures are gradually becoming prevalent. However, their micro-level impact on household carbon emissions remains unclear. This study is the first to combine household survey data with nighttime light imagery to dissect the role of polycentricity across multiple domains, including transportation, heating, and appliance usage.

---

## 2. Research Methods: Indicator Construction + Empirical Analysis

The methodology of this study is rigorous, integrating micro-level household survey data with nighttime light imagery data and employing an econometric model to analyze the effect of polycentric urban structures on household carbon emissions. Below is a detailed overview of the research methods:

---

### 2.1 Indicator Construction
>#### 2.1.1 Household Carbon Emission Data

- Data Source: The study uses data from the 2012 China Residential Energy Consumption Survey (CRECS). This survey covers demographic information, housing characteristics, household appliances, heating and cooling arrangements, transportation modes, electricity consumption, and more.  
- Carbon Emission Calculation: Based on household energy use records, the study calculates household direct carbon emissions, including emissions from transportation, heating, cooking, and appliance usage. The specific formula is:  
  $
  \text{Carbon Emission}_i = \sum_{m=1}^{M} \sum_{n=1}^{N} E_{i,m,n} \times EF_n
  $

  $
  E_{i,m,n} = power_{i,m,n} \times frequency_{i,m,n}\times duration_{i,m,n}\times livingdays_{i}
  $

  Here, \( E_{i,m,n} \) is the consumption of energy \( n \) by household \( i \) for activity \( m \), and \( EF_n \) is the carbon emission factor of energy \( n \).

  \( power_{i,m,n} \) represents the device’s output power, \( frequency_{i,m,n} \) the daily usage frequency, \( duration_{i,m,n} \) the length of each usage, and \( livingdays_{i} \) the actual number of days household \( i \) spent in the residence during 2012.

>#### 2.1.2 Measuring Polycentricity

- Data Source: The study uses nighttime light imagery data as a proxy for polycentricity. Nighttime light data can capture the geographical distribution of economic activities without being limited by administrative boundaries, thereby providing high reliability.  
- Polycentricity Indicator: The study measures polycentricity by calculating the weighted average distance of each county/district’s economic activities relative to the city center (CBD). The specific formula is:  
  $
  \text{Poly}_{j} = \sum_{i=1}^{n} \frac{l_{ij}}{L_{j}} \times \frac{Dis\_ CBD_{ij}}{CR_{j}}
  $

  \( l_{ij} \) denotes the brightness of pixel \( i \) in county/district \( j \), \( L_{j} \) is the total brightness in county/district \( j \), \( Dis\_ CBD_{ij} \) the distance from pixel \( i \) to the CBD, and \( CR_{j} \) is the city radius.

<br/><img src='/images/p1.jpg'>

---

### 2.2 Empirical Strategy

>#### 2.2.1 Baseline Regression Model

The study adopts a multiple linear regression model to analyze the impact of polycentricity on household carbon emissions. The baseline model is as follows:  
$
\ln(\text{CO2}_{ij}) = \alpha_0 + \alpha_1 \text{Poly}_{j} + \text{HouseC}_{ij}^\prime \alpha_2 + \text{CountyC}_{j}^\prime \alpha_3 + \epsilon_{ij}
$

- Dependent Variable:  
  \(\ln(\text{CO2}_{ij})\), the logarithm of the carbon emissions of household \( i \) in county/district \( j \).  
- Key Independent Variable:  
  \(\text{Poly}_{j}\), the polycentricity indicator for county/district \( j \).  
- Control Variables:  
  - Household Level: per capita income, household size, average age, education level, housing area, whether central heating is used, etc.  
  - County/District Level: per capita GDP, county/district area, etc.

<br/><img src='/images/p2.jpg' width="600">

>#### 2.2.2 Instrumental Variable (IV) Method

To address potential endogeneity issues (e.g., a bidirectional causal relationship between urban structures and carbon emissions), the study employs an instrumental variable (2SLS) approach:  
- Instrumental Variable: The 2000 polycentricity indicator is used as an instrument for the 2012 polycentricity measure. The rationale is that the city structure in 2000 is correlated with that in 2012 but is unlikely to be directly related to household carbon emissions in 2012.  
- First-Stage Regression:  
  $
  \widehat{\text{Poly}_{j}} = \gamma_0 + \gamma_1 \text{Poly}_{2000} + \text{HouseC}_{ij}^\prime \gamma_2 + \text{CountyC}_{j}^\prime \gamma_3 + v_{ij}
  $

- Second-Stage Regression:  
  $
  \ln(\text{CO2}_{ij}) = \beta_0 + \beta_1 \widehat{\text{Poly}_{j}} + \text{HouseC}_{ij}^\prime \beta_2 + \text{CountyC}_{j}^\prime \beta_3 + \psi_{ij}
  $

<br/><img src='/images/p5.jpeg'>

---

### 2.3 Robustness Checks

To ensure the reliability of the results, the study conducted the following robustness checks:  
1. Replacing the polycentricity indicator: using the “light-weighted Gini coefficient” (1 - Gini light) as an alternative polycentricity measure and re-running the regression.  
2. Data Trimming: trimming the explanatory and dependent variables at the 1% and 99% levels to reduce the influence of outliers.

---

### 2.4 Mechanism Analysis

The study further breaks down household carbon emissions to explore how polycentricity affects emissions through the following mechanisms:

>#### 2.4.1 Transportation Carbon Emissions  
- Influencing Factors: travel distance, travel frequency, transportation mode (private car usage).  
- Regression Model: using travel distance, travel frequency, and private car usage as dependent variables, analyzing the effect of polycentricity.

>#### 2.4.2 Household Energy Use Carbon Emissions  
- Influencing Factors: housing area, heating method (central heating or other), the number and usage duration of household appliances.  
- Regression Model: using heating carbon emissions, housing area, central heating usage rate, and appliance count and usage duration as dependent variables to analyze the impact of polycentricity.

---

### 2.5 Urban–Rural Differences Analysis

The study divides the sample into urban and rural households for separate regression analyses, exploring the heterogeneous impact of polycentricity on household carbon emissions. Additionally, it constructs an urban–rural carbon emission gap indicator (EmissionRatio) to examine how polycentricity affects the urban–rural emissions gap.

---

## 3. Key Findings: Polycentric Development Spurs Higher Carbon Emissions, with Significant Urban–Rural Differences

### 3.1 The “Carbon Emission Paradox” of Polycentric Cities

- Overall Effect: Polycentric structures significantly increase household carbon emissions, with rural areas seeing a larger increase (25% higher coefficient for rural areas compared to urban areas).  
- Mechanism Breakdown:  
  - Transportation: Urban residents have shorter commuting distances, but increased travel frequency and private car use offset emission reduction. Rural residents, due to limited public transportation, rely more on private cars, leading to a sharp rise in transportation emissions.  
  - Household Energy: Heating (driven by larger housing areas and the spread of central heating) and appliance usage (the increased number of household appliances and longer usage in rural areas) emerge as key emission sources.

<br/><img src='/images/p3.jpg'>

### 3.2 Narrowing the Urban–Rural Emission Gap

Polycentric development raises living standards in rural areas (e.g., greater appliance ownership, better heating), causing rural household carbon emissions to grow faster and narrowing the urban–rural emission gap. This finding offers a new perspective for low-carbon policies under the goal of “common prosperity.”

---

## 4. Policy Implications: Balancing Efficiency and Equity in Polycentric Planning

1. Transportation Optimization:
   - Strengthen urban–rural public transportation networks to curb reliance on private cars.  
   - Develop “15-minute living circles” in sub-centers to reduce long-distance travel needs.

2. Clean Heating:
   - Promote industrial waste heat heating in northern regions and encourage the transition from coal to electricity/gas in southern regions.  
   - Reinforce insulation in new buildings to reduce heating energy consumption.

3. Improving Appliance Energy Efficiency:
   - Expand subsidies for energy-efficient appliances in rural areas, accelerating the replacement of outdated appliances.  
   - Develop distributed energy (e.g., rooftop solar) to lower grid carbon emissions.

4. Balancing Functional Layout:
   - Avoid single-function sub-centers; ensure supporting facilities for education and healthcare, reducing cross-region travel demands.

---

## 5. Research Value: Micro-Level Data Reveals Macro-Level Paths

This paper breaks through the limitations of traditional city-level carbon emission analyses, using micro-level household data to unveil the complex impacts of polycentric structures. The discovery of significant urban–rural differences is especially crucial, suggesting that policy-making should be context-specific—cities should focus on optimizing transportation and building energy efficiency, while rural areas need to simultaneously improve living standards and spread low-carbon technologies.

Future Outlook: As China advances toward its “dual carbon” goals, further empirical research is needed on how polycentric cities balance development efficiency and emission reduction responsibilities. This study provides a methodological framework and policy entry points for future exploration.

---

Paper Information:  
Liu, J., Long, F., Chen, L., Zheng, L., & Mi, Z. (2025). The role of polycentric urban structures in shaping low-carbon lifestyles. Cities, 157, 105616.  
DOI: 10.1016/j.cities.2024.105616
