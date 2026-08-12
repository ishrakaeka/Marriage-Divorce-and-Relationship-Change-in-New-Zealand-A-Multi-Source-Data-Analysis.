# Marriage, Divorce & Relationship Change in New Zealand

Project Overview:
This project investigates marriage, divorce, and relationship change in New Zealand through an integrated, multi-source data-analysis approach. The project combines official New Zealand statistics, legal information, demographic indicators, and government open-data metadata to examine how formal relationships have changed over time and the broader social, demographic, and legal factors that provide context for those changes.

The analysis is centred on eight research questions (RQ1–RQ8) and uses four complementary data sources:
Data Source	Type	Period
1	Statistics New Zealand — 5 CSV files	Static local CSV	2005–2020
2	Community Law NZ — 3 pages	Dynamic web scraping	Runtime
3	Gapminder Systema Globalis	Dynamic remote file retrieval	2005–2022
4	NZ Government Open Data Portal	Dynamic CKAN REST API / JSON	Runtime
The project demonstrates how heterogeneous data sources can be collected, cleaned, integrated, analysed, and interpreted to answer complex social research questions.

Data Sources:
1. Statistics New Zealand
The project uses five Stats NZ CSV datasets as the primary statistical source.
Coverage: 2005–2020
The datasets provide the core quantitative evidence for analysing:
Marriage counts
Divorce counts
Marriage rates
Divorce rates
Median age
Gender
Relationship type
Annual trends
The CSV files were stored locally and processed using Python.
Because the datasets contained differences in column names, row structures, and year coverage, substantial cleaning and harmonisation were required before integration.

2. Community Law NZ
Three publicly accessible Community Law NZ pages were analysed to provide legal context for the statistical findings.
The legal analysis focused on:
Divorce requirements
Separation
Two-year separation requirement
Family Court
Family Proceedings Act 1980
Relationship property
Equal sharing
Property division
Relationship dissolution
Legal content was retrieved dynamically through web scraping and processed using a keyword-based classification approach.
3. Gapminder Systema Globalis
Gapminder Systema Globalis data was retrieved programmatically during notebook execution.
Coverage: 2005–2022
The analysis uses demographic indicators including:
Female life expectancy
Male life expectancy
Crude death rate / mortality
The remote data was filtered for New Zealand and the required year range before being combined with the domestic relationship statistics.
This approach demonstrates reproducible runtime data retrieval rather than relying entirely on manually downloaded files.
4. NZ Government Open Data Portal
The NZ Government Open Data Portal was accessed through its CKAN REST API.
The API returns structured JSON metadata that can be queried programmatically.
Official API documentation:
NZ Government Open Data Portal CKAN API
The API was used to demonstrate:
Programmatic metadata retrieval
Open-data catalogue discovery
JSON processing
API-based data workflows
No login, registration, or API key was required for the public metadata access used in this project.

Executive Summary:
The analysis shows that both marriage and divorce rates declined between 2005 and 2020, with the decline in marriage being more pronounced than the decline in divorce.
At the same time, the median age at marriage and divorce increased across gender groups, indicating that New Zealanders were generally entering and leaving formal relationships later than in the earlier part of the study period.
The 2013 legalisation of same-sex marriage represents an important structural change. It expanded the population able to enter legally recognised marriage and produced a measurable change in the composition of formal unions captured in official statistics.
The legal analysis found that divorce in New Zealand generally requires a minimum two-year separation and a Family Court application under the Family Proceedings Act 1980. The analysis also identified the equal-sharing framework under the Property (Relationships) Act 1976 as an important feature of relationship-property division.
The demographic analysis examined the association between rising female life expectancy, mortality trends, and relationship dissolution. The findings provide demographic context for the increasing age at divorce and broader changes in relationship patterns.
Overall, the analysis suggests that declining marriage and divorce rates should not simply be interpreted as evidence of increasing relationship instability. Instead, they appear within a broader process of structural social and demographic change, including later marriage, later divorce, changing relationship types, changing life expectancy, and legislative change.

Reflective Summary:
The project developed through several distinct stages: data collection, cleaning, integration, analysis, and interpretation.
One of the most technically challenging aspects was preparing the five Stats NZ CSV files for analysis. The datasets contained inconsistent column naming, different year ranges, and varying row structures. These differences required careful harmonisation before meaningful comparisons could be performed.
The Gapminder data introduced another integration challenge because the indicators were retrieved programmatically from remote CSV files. The data needed to be filtered by country and year before being combined with the New Zealand relationship statistics.
The Community Law NZ analysis required a different approach again. Unlike the structured statistical datasets, legal information was available as unstructured text. A keyword-based classifier was therefore developed to identify and categorise relevant legal themes.
These challenges demonstrated that data preparation and integration are substantive analytical activities, rather than simple preliminary tasks.
Another important learning outcome was understanding the limitations of quantitative analysis. Stats NZ statistics provide strong evidence about what is happening, but they do not necessarily explain why. Legal analysis added institutional context that would otherwise remain invisible.
The correlation analyses also reinforced the distinction between association and causation. Statistically significant relationships provide evidence that variables move together, but they do not demonstrate that one variable causes another.
Overall, the project strengthened my ability to:
Work with heterogeneous datasets.
Clean and harmonise real-world data.
Integrate static and dynamic data sources.
Retrieve data programmatically.
Analyse structured and unstructured information.
Apply statistical techniques appropriately.
Interpret correlations cautiously.
Combine quantitative and qualitative evidence.
Communicate findings in a social-research context.

Technologies Used:
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Requests
BeautifulSoup
Jupyter Notebook
REST APIs
CKAN REST API

Conclusion:
This project demonstrates how multiple public data sources can be integrated to investigate complex social questions surrounding marriage, divorce, and relationship change in New Zealand.
Across eight research questions and nine analytical techniques, the project combines statistical trends, demographic indicators, legal text, and open-data metadata.
The overall findings suggest that declining marriage and divorce rates are better understood as part of broader structural change rather than simply as evidence of relationship instability.
The most important changes include:
Declining marriage rates.
Declining divorce rates.
Increasing median age at marriage.
Increasing median age at divorce.
Changing relationship composition following same-sex marriage legalisation.
Increasing life expectancy.
Changing legal and institutional contexts.
The project ultimately demonstrates that meaningful social-data analysis requires more than statistical calculations. Data preparation, source integration, legal and demographic context, methodological caution, and ethical data collection are all essential components of reliable analysis.
