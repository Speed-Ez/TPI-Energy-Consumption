# TPI-Energy-Consumption
**Analysis of TPI regional power consumption data**

Energy consumption data can tell powerful stories about how regions grow, industries operate, and demand shifts over time. I analyzed TobiPower Innovations (TPI) hourly energy usage dataset, which spans multiple companies across the Western Interconnection grid.

---
### Report Dashboard 
[CLICK HERE](https://app.powerbi.com/view?r=eyJrIjoiZjU2OTEzMDktMDQwYi00M2IyLWI1ODAtOWU1Njk2ZDZhMjJlIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9)

---
### **🔧 Data Preprocessing**

The project began with preparing the raw CSV files for analysis:

- **`Loaded CSV Files`**: Combined 12 company datasets using pandas.
- **`Datetime Conversion`**: Standardized all Datetime columns to proper datetime format.
- **`Optimization`**: Converted Megawatt columns from int64 → int32 for performance and smaller file size.
- **`Power BI Transformation`**: Imported the 12 CSVs into Power Query Editor, appended them into a single unified table (1_TPI_Combined), and unpivoted to a long format for flexible analysis.
- **`Efficiency Step`**: Disabled the original 12 tables from the report interface to keep the model lean.

Key Point: A single, unified dataset made it possible to run consistent analysis, including YoY MW change.

---

### **📐 DAX Measures**

I created measures to capture core insights:

- **`Avg Daily MW`** → Average daily consumption per company.
- **`Avg Hourly MW`** → Average usage per hour.
- **`Max Hourly MW`** → Peak hourly demand.
- **`Total MW`** → Cumulative consumption.
- **`YoY MW Change`** → Percentage change in total MW vs. same period last year.

---

### **Visuals**

The dashboards highlighted different perspectives of consumption:

- **`Line Chart`** → YoY MW change by company/year.
- **`Bar Chart 1`** → Total MW usage by company/region.
- **`Bar Chart 2`** → Max Hourly MW usage by company.
- **`Matrix Heatmap`** → Average hourly usage by company, showing peak vs. regular hours.

---

### **📊 Key Insights**

- PJME leads consumption with peaks at 62k MW (08-Feb-2006), an hourly average of 32k MW, and a total of 4.69B MW — crucial for YoY analysis.
- AEP and COMED follow strongly, with peaks at 25.70k MW (AEP) and 23.75k MW (COMED). Their hourly averages of 15.5k MW and 11.42k MW highlight significant load for capacity planning.
- PJM_Load (pre-2002) showed a peak of 54.03k MW, reflecting historical YoY shifts.
- Evidence suggests PJM_Load was the sole distribution company before 2002, confirming that regions/companies evolved over time.

---

### **⏰ Hourly Patterns**

- **`Peak Hours (10:00–22:00)`**: Driven by industrial/commercial activity and cooling/heating demands.
- **`Regular Hours (0:00–9:00)`**: Lower usage, reflecting reduced activity at night and early morning.

PJM_Load and PJME: Showed the sharpest peaks, indicating their heavy role in demand.

---

### **🚀 Recommendations**

- Prioritize PJME in Capacity Planning → Plan for its 62k MW peaks and 32k MW averages, using YoY trends to forecast future demand.
- Optimize Peak Hours (10:00–22:00): Deploy efficiency programs (e.g., demand response) to reduce grid strain, especially for AEP and COMED.
- Leverage YoY Insights: Identify companies with rising usage (e.g., PJME’s growth) for targeted infrastructure investments.
- Focus on High-Demand Areas: Prioritize PJME, AEP, COMED, and PJM_Load to stabilize grid operations and support expansion.

---

### **✨ Closing Thought**

This project shows how data preprocessing, DAX measures, and visualization in Power BI can turn raw consumption logs into strategic insights for energy planning. By understanding not just how much energy is used, but also when, where, and by whom, organizations can prepare smarter policies, optimize capacity, and manage resources sustainably.
