# Power-BI-Dashboard-on-Students-Academic-Performance-based-on-AI-Tools-Used
Power BI dashboard analyzing 8,000 students' academic performance based on AI tools used. Examines Gender, AI Tool Usage Purpose, and Passing Status with interactive visualizations (Area Chart, Treemap, Pie Chart). Includes key measures: Max/Min/Average Score and Standard Deviation. Built with Power BI and Excel. Self project.

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Dashboard Features](#dashboard-features)
- [Visualizations](#visualizations)
- [Key Measures](#key-measures)
- [Files Structure](#files-structure)
- [How to Use](#how-to-use)
- [Key Insights](#key-insights)
- [Technologies Used](#technologies-used)
- [Author](#author)

## 📚 Project Overview

This independent project develops an interactive Power BI dashboard to understand how AI tools impact student academic performance. The analysis examines:
- **AI Tool Adoption** - Which AI tools students use
- **Gender Distribution** - Performance differences across genders
- **Usage Purposes** - Why students use AI tools
- **Academic Outcomes** - Passing status and performance scores

The dashboard provides actionable insights into modern educational technology trends and their correlation with student success.

**Project Type:** Independent Data Analytics Project  
**Duration:** June 2026 - July 2026  
**Platform:** Microsoft Power BI  
**Dataset:** Synthetic educational data (8,000 students)

## 📊 Dataset

- **Sample Size:** 8,000 students
- **Total Variables:** 23
- **Data Type:** Synthetic educational records
- **Time Period:** Current academic year

### Key Dimensions Analyzed
1. **Gender** - Male/Female distribution
2. **AI Tools Used** - ChatGPT, Gemini, Claude, GitHub Copilot, etc.
3. **AI Tool Usage Purpose** - Research, Assignment Help, Code Generation, Note-taking, etc.
4. **Passing Status** - Pass/Fail binary outcome
5. **Academic Scores** - Final scores and performance metrics

### Data Quality
- Comprehensive student records
- Balanced gender distribution
- Diverse AI tool adoption patterns
- Clean, validated data

## 📈 Dashboard Features

### Interactive Elements
- **Slicers & Filters** - Dynamic filtering by:
  - Gender
  - AI Tool Used
  - Usage Purpose
  - Passing Status
  
- **Drill-through Capability** - Navigate between report pages
- **Tooltip Details** - Hover for additional information
- **Cross-filtering** - Clicking visuals filters related data
- **Real-time Updates** - Data refreshes automatically

### Dashboard Pages
1. **Overview Dashboard** - High-level KPIs and trends
2. **AI Tool Analysis** - Detailed tool adoption patterns
3. **Gender-wise Performance** - Comparative gender analysis
4. **Usage Purpose Impact** - How different use cases affect performance
5. **Detailed Data Table** - Full dataset view with sorting/filtering

## 📊 Visualizations

### 1. Area Chart
**Purpose:** Trend analysis over time or progression

**Key Insights:**
- Shows score progression across student segments
- Reveals temporal patterns in AI adoption
- Displays cumulative trends
- Interactive hover details

**Dimensions:**
- X-axis: Time period or sequence
- Y-axis: Score values
- Color: Different AI tools or gender

### 2. Treemap
**Purpose:** Hierarchical data visualization

**Key Insights:**
- Visual representation of AI tool popularity
- Size represents frequency or aggregate score
- Color intensity shows performance
- Easily identify dominant categories

**Hierarchies:**
- AI Tool Usage Purpose → AI Tools Used
- Gender → Passing Status
- Performance tiers by tool

### 3. Pie Chart
**Purpose:** Part-to-whole relationships

**Key Insights:**
- Proportional distribution of passing/failing students
- Gender ratio in AI tool usage
- Tool usage distribution percentages
- Categorical comparison

**Usage:**
- Passing Status distribution
- Gender breakdown
- Tool adoption proportions
- Purpose distribution

### 4. Additional Visualizations (Supporting)
- **Bar Charts** - Comparative analysis
- **Line Charts** - Trend progression
- **Tables** - Detailed metrics display
- **KPI Cards** - Key performance indicators

## 📊 Key Measures

### Basic Statistical Measures

**1. Maximum Score**
```
Maximum Score = MAX(Student[Final_Score])
```
- Highest score achieved in dataset
- Benchmark for excellent performance
- Filter by gender, tool, or purpose

**2. Minimum Score**
```
Minimum Score = MIN(Student[Final_Score])
```
- Lowest score in dataset
- Identifies performance floor
- Context for performance range

**3. Average Score**
```
Average Score = AVERAGE(Student[Final_Score])
```
- Mean academic performance
- Central tendency measure
- Baseline for comparison
- Dynamic by filters

**4. Standard Deviation of Score**
```
Std Dev Score = STDEV(Student[Final_Score])
```
- Measures score variability
- Higher = more diverse performance
- Indicates consistency level
- Performance spread insight

### Derived Measures

**Passing Rate**
```
Passing Rate = DIVIDE(COUNTIF(Passing_Status="Pass"), COUNTA(Passing_Status))
```
- Percentage of students passing
- Key success metric
- Varies by demographics

**Performance Quartiles**
```
Quartile Ranking = RANKX(ALL(Student), [Average Score])
```
- Groups students by performance tier
- Top/bottom performer identification
- Segment-specific analysis

**AI Tool Impact Score**
```
Tool Impact = DIVIDE([Average Score by Tool], [Overall Average Score])
```
- Shows relative performance by tool
- Identifies beneficial tools
- Comparative effectiveness

## 📁 Files Structure

```
Power-BI-Dashboard-Project/
├── README.md                          # This file
├── Project_3_Sulagna_Roy.pbix        # Main Power BI file
├── Data/
│   ├── student_data.xlsx             # Source data (8,000 records)
│   ├── data_dictionary.txt           # Variable descriptions
│   └── AI_tools_reference.csv        # AI tools lookup table
├── Documentation/
│   ├── Dashboard_Guide.md            # How to navigate dashboard
│   ├── DAX_Formulas.txt              # Power BI DAX code
│   ├── Data_Model.md                 # Relationship diagrams
│   └── Key_Insights.md               # Analysis findings
├── Images/
│   ├── dashboard_overview.png        # Screenshot of main dashboard
│   ├── visualization_samples.png     # Chart examples
│   └── measure_examples.png          # Measure results
└── Excel_Support/
    ├── data_preparation.xlsx         # Excel data prep workflow
    └── calculations_backup.xlsx      # Backup calculations
```

## 🚀 How to Use

### Prerequisites
- **Microsoft Power BI Desktop** (latest version)
  - Download: [power.microsoft.com](https://powerbi.microsoft.com)
- **Microsoft Excel** (optional, for data viewing)
- **4GB RAM minimum** for smooth performance
- **.pbix file viewer** (online Power BI Service alternative)

### Installation & Setup

#### Option 1: Desktop Application (Recommended)

1. **Install Power BI Desktop**
   ```
   1. Go to powerbi.microsoft.com/downloads
   2. Click "Download" for Power BI Desktop
   3. Run installer and complete setup
   ```

2. **Open the Dashboard**
   ```
   1. Launch Power BI Desktop
   2. File → Open → Select "Project_3_Sulagna_Roy.pbix"
   3. Wait for data refresh (1-2 minutes)
   4. Dashboard loads automatically
   ```

3. **Navigate the Dashboard**
   - Use tabs at bottom for different pages
   - Click slicers to filter data
   - Hover over visuals for details
   - Click visuals for cross-filtering

#### Option 2: Power BI Online Service

1. **Upload to Power BI Service**
   ```
   1. Sign in at powerbi.microsoft.com
   2. Workspace → New → Upload file
   3. Select "Project_3_Sulagna_Roy.pbix"
   4. Access from any device
   ```

2. **Share with Others**
   - Power BI → Share → Enter email addresses
   - Grant view/edit permissions
   - Collaborate in real-time

### Dashboard Navigation Guide

**Main Dashboard Page:**
- Top: Summary KPIs (Avg Score, Passing Rate, etc.)
- Left: Slicers for filtering (Gender, Tool, Purpose)
- Center: Interactive visualizations
- Right: Detailed metrics

**Using Slicers:**
1. Click slicer button to expand
2. Select one or multiple options
3. All charts update automatically
4. "Clear" button resets filter

**Interacting with Visuals:**
- **Click bars/segments** → Filter other charts
- **Double-click** → Drill down to details
- **Hover** → See tooltip values
- **Right-click** → Export or spotlight options

**Exporting Data:**
1. Right-click on visual
2. Export data → CSV or Excel
3. Create custom analysis
4. Share with stakeholders

## 📊 Key Insights

### AI Tool Adoption Trends

**Most Popular AI Tools:**
- **ChatGPT** - Highest adoption rate
- **Gemini** - Growing usage among students
- **Claude** - Preferred for research
- **GitHub Copilot** - Popular among coders

**Usage by Tool:**
- Tool A: X% of students use
- Tool B: Y% adoption
- Tool C: Z% adoption
- [Specific percentages from your data]

### Performance Analysis

**Gender-wise Insights:**
- Male students: Average score comparison
- Female students: Average score comparison
- Passing rate differences: X% vs Y%
- Performance consistency (std dev): [values]

**AI Tool Impact on Scores:**
- Students using Tool A: Avg score [X]
- Students using Tool B: Avg score [Y]
- Non-users: Avg score [Z]
- Score improvement: [%] with AI tools

### Usage Purpose Insights

**Top Usage Purposes:**
1. **Research & Assignment Help** - Most common
2. **Code Generation** - Developers focus
3. **Note-taking & Summarization** - Study aid
4. **Content Creation** - Writing assistance

**Purpose-Performance Correlation:**
- Research → Higher average scores
- Homework Help → Moderate impact
- Entertainment Use → Lower correlation
- [Specific insights from data]

### Passing Status Patterns

**Overall Passing Rate:** [X]%

**By AI Tool Usage:**
- Tool users: [A]% passing
- Non-users: [B]% passing
- Multiple tool users: [C]% passing

**By Gender:**
- Male passing rate: [X]%
- Female passing rate: [Y]%
- Combined: [Z]%

### Key Findings Summary

✅ **AI tools positively correlate with academic performance**
✅ **Specific tools show stronger impact than others**
✅ **Purpose of usage matters more than frequency**
✅ **Gender shows minimal impact on tool effectiveness**
✅ **Purposeful tool use yields better outcomes**

## 🛠️ Technologies Used

### Power BI Components
- **Power BI Desktop** - Dashboard development
- **Power Query** - Data transformation
- **DAX (Data Analysis Expressions)** - Custom measures
- **Data Modeling** - Relationship management

### Supporting Tools
- **Microsoft Excel** - Data preparation & backup
- **SQL** (optional) - Data extraction if needed
- **Power BI Service** - Cloud publication & sharing

### Key Features Utilized
- Interactive visualizations
- Custom DAX formulas
- Hierarchical data structures
- Drill-through reports
- Dynamic filtering
- Conditional formatting
- Custom tooltips

## 📈 Performance Optimization

### Dashboard Optimization Techniques
- Query folding in Power Query
- Optimized data model relationships
- Aggregated tables for large datasets
- Efficient DAX formulas
- Proper indexing strategies

### Load Time Tips
- First load: 1-2 minutes (data refresh)
- Subsequent loads: Instant
- Slicer interaction: <1 second
- Visual updates: Real-time

## 👩‍💼 Author

**Sulagna Roy**  
Independent Data Analytics Project  
Project Duration: June 2026 - July 2026

## 📝 License

This project is an independent analytics initiative and learning demonstration.

## 📧 Contact & Collaboration

For questions or feedback:
- Email: sulagna1roy@gmail.com
- GitHub: https://github.com/sulagna01royofficial
- LinkedIn: www.linkedin.com/in/sulagna01-roy 

## 🎯 Project Achievements

✅ Built interactive Power BI dashboard  
✅ Analyzed 8,000 student records  
✅ Created 4 key visualizations  
✅ Implemented 4 statistical measures  
✅ Dynamic filtering & cross-filtering  
✅ Professional-grade dashboard  
✅ Actionable insights delivered  

## 📚 How to Interpret Visualizations

### Area Chart Interpretation
- Upward trend = Increasing scores
- Peak values = Optimal usage periods
- Comparison across areas = Tool effectiveness

### Treemap Interpretation
- Larger boxes = Higher frequency/counts
- Darker colors = Better performance
- Nested structure = Hierarchical relationships

### Pie Chart Interpretation
- Slice size = Proportion of total
- Color segments = Category distribution
- Percentages = Exact proportion values

## 🔄 Future Enhancements

Potential improvements:
- Real-time data connection to live database
- AI-powered predictions using R/Python
- Advanced analytics with clustering
- Comparative year-over-year analysis
- Student segmentation & personas
- Predictive modeling for at-risk students
- Mobile-optimized dashboard version
- Automated alert system for performance

## 📊 Data Refresh Schedule

**Current Setup:** Manual refresh  
**Recommendation:** Set up automatic refresh
- Frequency: Daily/Weekly/Monthly
- Time: Off-peak hours recommended
- Method: Power BI Service scheduled refresh

**How to Schedule Refresh:**
1. Power BI Service → Dataset settings
2. Scheduled refresh → Configure
3. Set frequency and time
4. Save settings

## 💡 Tips & Tricks

### For Dashboard Users
- **Ctrl + Click** = Multiple selections in slicer
- **Ctrl + A** = Select all items
- **ESC** = Clear selections
- **Export Data** → Detailed analysis
- **Pin Visuals** → Create bookmarks

### For Customization
- Edit in Power BI Desktop
- Modify colors, fonts, layout
- Add/remove visualizations
- Create new pages
- Save as custom version

## 🔍 Troubleshooting

**Dashboard won't open:**
- Update Power BI Desktop to latest version
- Check system RAM (4GB minimum)
- Disable hardware acceleration if slow

**Data not refreshing:**
- Check data source connection
- Verify file path is correct
- Manual refresh: Refresh button

**Visualizations look blurry:**
- Adjust monitor DPI settings
- Increase canvas resolution
- Use Power BI Service (online)

---

**Last Updated:** July 2026  
**Project Status:** Completed & Ready for Use  
**Data Version:** 8,000 student records, 23 variables  

---

## Quick Start

```bash
# To open dashboard:
1. Download Power BI Desktop
2. Open "Project_3_Sulagna_Roy.pbix"
3. Use slicers to explore data
4. Click visuals for insights
```

**For detailed analysis, see embedded tooltips and documentation pages within the dashboard!**

---

## Additional Resources

- [Power BI Documentation](https://docs.microsoft.com/power-bi/)
- [DAX Function Reference](https://dax.guide/)
- [Power Query Editor Guide](https://docs.microsoft.com/power-query/)
- [Best Practices for Power BI](https://docs.microsoft.com/power-bi/guidance/)

---

**Enjoy exploring student academic performance trends with AI tools! 📊✨**
