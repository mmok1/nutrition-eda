# Process Writeup
## Link to Video Explanation: 
https://youtu.be/WXKxZOkidhI
## Project Selection and Execution
Our team was motivated by a shared interest in understanding how health conditions and quality of life vary across different demographic groups. We were particularly drawn to topics such as Food Insecurity & Hunger, Obesity of Children & Adolescents, and Consumption of Added Sugars, given their significant public health impact and the potential to reveal underlying disparities. We aimed to explore these issues through multiple lenses—specifically race, age, and education level—to gain a comprehensive understanding of how different populations experience similar challenges.
Initially, our plan was to highlight key figures from the datasets using estimated values alone (via the “Estimates” variable). However, after preliminary exploration, we realized that incorporating disparity metrics, such as the Disparity Rate Ratio, would allow us to capture relative differences between groups, adding depth and nuance to our analysis. This approach ultimately enabled us to create a dashboard that presents both absolute prevalence and relative disparities, revealing insights that would otherwise remain hidden. Our goal was to develop an interactive analytical dashboard in Tableau, supported by clear documentation, that empowers users to explore these disparities and understand which groups face the most significant challenges.
## Assumptions and Limitations
Our analysis assumes a consistent population base across datasets, though in practice, differences in survey populations or timeframes may affect comparability. A key limitation we encountered was the presence of duplicate entries and data points with insufficient detail or questionable reliability. We addressed this by filtering out incomplete or low-quality data, though this necessarily narrowed the scope of our analysis and affected the confidence we could place in some trends. Additionally, some groups had estimates but lacked calculated disparity rates or rate ratios; we chose not to exclude these groups entirely, as comparing their estimates still offered valuable insights even when disparity metrics were unavailable.
Audience, Questions, and Usefulness
Target Audience: This project is intended for policymakers, researchers, and community organizations focused on health equity and disparities.
## Key Questions
- Which demographic groups experience the highest levels of food insecurity and other health concerns?
- Where are the most significant disparities found, and how do they compare to absolute prevalence?
- How can this data guide interventions and resource allocation?


## Usefulness and Alignment
Our dashboard is designed to help users identify priority areas for intervention, allocate resources effectively, and guide further research into the root causes of health inequities. By visualizing both absolute prevalence (Estimates) and relative disparities (Disparity Rate Ratio), the dashboard supports data-driven decision-making aligned with the audience’s needs.
While our analysis reveals clear patterns of disparity, it is constrained by the available data and assumptions of consistent population bases. Additional data—especially on underlying causes and qualitative insights—would enhance our ability to fully answer the underlying questions and support even more targeted recommendations.
## Data Cleaning and Preparation
We sourced our data from the CDC website, using four separate datasets: Obesity, Physical Activity, Food Insecurity, and Added Sugar Consumption. Since all four datasets shared the same column structure, we concatenated them into a single dataset. This approach streamlined our filtering process in Tableau and made data exploration more efficient and consistent. In addition to our CDC datasets, for supplemental documents, we sourced an average income table across different  races from DQYDJ (external website: https://dqydj.com/income-by-race/) to help us better understand the relationship between those two variables.
## Data cleaning steps included:
Removing all DNC (Did Not Collect) and DNS (Did Not Specify) entries to ensure data integrity.


Standardizing naming conventions, particularly consolidating “Race/Ethnicity” and “Race/Ethnicity (of household reference)” into a single, unified category.


Filtering out duplicate entries and data points with insufficient detail or questionable reliability.


Conducting validation checks to confirm that calculations remained consistent across demographic groups, ensuring the accuracy of both estimates and disparity metrics.


These steps helped ensure the data imported into Tableau was reliable and ready for visualization.
## Potential Additional Analyses
Given more time and additional data, we would have expanded our analysis in several key ways:
- Additional Health Concerns: Exploring a wider range of public health conditions beyond food insecurity, obesity, and added sugar consumption—such as chronic diseases, mental health, and access to healthcare—would provide a more holistic understanding of health disparities.
- Comorbidity Analysis: Examining how health disparities intersect and compound one another would reveal critical insights into how multiple health challenges can exacerbate risks, particularly for already vulnerable populations.
- Geographic Analysis: Incorporating spatial analysis—such as mapping disparities across states, counties, or urban vs. rural areas—would uncover regional patterns and help policymakers allocate resources more effectively. This would be especially useful for identifying areas where multiple disparities cluster together.
- Policy and Intervention Evaluation: Exploring current public-sector initiatives aimed at improving health equity would allow us to assess their effectiveness and identify gaps or successes. Additionally, developing “success scores” for these initiatives could provide benchmarks for future progress and help guide policymakers in refining resource allocation strategies.


## Tool Summaries
### Tableau Dashboard
Our Tableau dashboard presents an analysis of key health concerns, including Food Insecurity & Hunger, Obesity of Children & Adolescents, and Consumption of Added Sugars. It visualizes overall rates and disparities in outcomes using metrics like Disparity Rate and Disparity Rate Ratio. The quadrant chart highlights which groups experience the greatest disparities and prevalence, helping to guide targeted interventions. Additional charts provide detailed breakdowns by demographic group to support health equity efforts. Note that some groups may appear in the estimates bar graph but not in the Disparity Rate Ratio bar graph or scatter plot; this occurs because those groups had estimates but lacked disparity metrics. We chose to retain these data points, as their estimates still provide valuable insights.
### Excel/PowerPoint
There are multiple factors that affect the quality of life and food of people from different backgrounds. Understanding the relationships of variables like income, age groups, race, and education levels with CDC datasets that talk about children obesity, sugar consumption, and food insecurity/hunger can help the policymakers, researchers, and community organizations in identifying target areas where interventions are most needed. Thus, there is a necessity to have an informative tool, like our dashboard, to aid in potentially guiding further investigation or resource allocation.
### Python Notebook
The Python notebook was used for exploratory data analysis, cleaning, and visualization to support and validate key findings from the CDC datasets. We used libraries like pandas, seaborn, and plotly to filter demographic groups, identify trends, and create static and interactive charts. Key outputs included a line chart of food insecurity by race/ethnicity, a grouped bar chart of childhood obesity by sex, and a faceted comparison of obesity and added sugar consumption. These visuals were exported as HTML files and helped guide the design of our Tableau dashboard.
## Download and View Interactive Graphs:
- [Added Sugar vs Obesity (NWS-10, NWS-04)](https://drive.google.com/uc?export=view&id=1vVhd9MkpJh4aK6WQhUUK7wL7J035YFxI)
- [Top 4 Ethnicities by Food Insecurity (NWS-01)](https://drive.google.com/uc?export=view&id=1PI0J62P2g49zmhqSnK-K7zaMDx4t06KV)
- [Childhood Obesity by Sex and Time Period (NWS-04)](https://drive.google.com/uc?export=view&id=1MSLi-05D-NzzAAswoaJ3kqu59TBGkIXk)
## Extra Credit Opportunities
In Tableau, we used a calculated field to create different colors in ever quandrant based on every value on dashboard. Inkscape was used to polish Excel graphs and fix alignment issues. Unpolished graphs are in the excel file, while polished graphs are in the Powerpoint Presentation. We also published Plotly graphs to make HTML files, publishing to websites, which was beyond the scope of what we learned in class. 
## Use of ChatGPT/AI
We leveraged ChatGPT primarily to refine our ideas, enhance the narrative, and ensure our documentation was clear and cohesive. AI assistance also helped us implement dynamic reference lines and calculated fields in Tableau, and guided us in applying dynamic titles that respond to selected filters and column aliases (the aliases part was new to us). Additionally, ChatGPT provided best practices for presenting disparity metrics in an accessible way, including layout suggestions and clear definitions. ChatGPT was also used to help us debug Python code and help design Plotly graphs.
