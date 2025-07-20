# Titanic Dataset - Exploratory Data Analysis

## 📊 Project Overview

This project provides a comprehensive Exploratory Data Analysis (EDA) of the famous Titanic disaster dataset. The analysis aims to uncover patterns, relationships, and insights about passenger survival factors during the tragic sinking of RMS Titanic on April 15, 1912.

The sinking of the Titanic is one of the most infamous shipwrecks in history. During her maiden voyage, the Titanic collided with an iceberg, resulting in the death of 1502 out of 2224 passengers and crew. This analysis explores what factors influenced passenger survival rates.

## 🎯 Objectives

- **Data Understanding**: Explore the structure and characteristics of the Titanic dataset
- **Data Cleaning**: Handle missing values, outliers, and data inconsistencies
- **Pattern Discovery**: Identify key factors that influenced passenger survival
- **Visualization**: Create meaningful charts and graphs to communicate findings
- **Statistical Analysis**: Perform statistical tests and correlation analysis

## 📁 Project Structure

```
ExploratoryDataAnalysisTitanicDataset/
│
├── README.md                    # Project documentation
├── EDA.ipynb                   # Jupyter notebook with complete analysis
├── TitanicDataset.csv          # Raw dataset
├── .gitignore                  # Git ignore file
└── .gitattributes              # Git attributes file
```

## 📋 Dataset Description

The Titanic dataset contains information about 891 passengers (out of 2224 total passengers and crew). Each row represents a passenger with the following features:

| Variable | Definition | Key |
|----------|------------|-----|
| **PassengerId** | Unique identifier for each passenger | Integer |
| **Survived** | Survival status | 0 = No, 1 = Yes |
| **Pclass** | Ticket class (proxy for socio-economic status) | 1 = 1st, 2 = 2nd, 3 = 3rd |
| **Name** | Passenger name | String |
| **Sex** | Gender | male/female |
| **Age** | Age in years | Float (fractional if less than 1) |
| **SibSp** | Number of siblings/spouses aboard | Integer |
| **Parch** | Number of parents/children aboard | Integer |
| **Ticket** | Ticket number | String |
| **Fare** | Passenger fare (in British pounds) | Float |
| **Cabin** | Cabin number | String |
| **Embarked** | Port of embarkation | C = Cherbourg, Q = Queenstown, S = Southampton |

### Data Source
- **Source**: Kaggle Titanic Competition
- **Size**: 891 rows × 12 columns
- **Format**: CSV (Comma Separated Values)

## 🛠️ Technologies & Libraries

### Programming Language
- **Python 3.x**

### Core Libraries
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computing
- **matplotlib**: Data visualization
- **seaborn**: Statistical data visualization
- **scipy**: Statistical analysis

### Development Environment
- **Jupyter Notebook**: Interactive development environment

## 🚀 Getting Started

### Prerequisites

Ensure you have Python 3.x installed on your system. You can download it from [python.org](https://www.python.org/).

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/darshanPC25/ExploratoryDataAnalysisTitanicDataset.git
   cd ExploratoryDataAnalysisTitanicDataset
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv titanic_eda
   source titanic_eda/bin/activate  # On Windows: titanic_eda\Scripts\activate
   ```

3. **Install required dependencies**
   ```bash
   pip install pandas numpy matplotlib seaborn scipy jupyter
   ```

   Or create a `requirements.txt` file with:
   ```
   pandas>=1.3.0
   numpy>=1.21.0
   matplotlib>=3.4.0
   seaborn>=0.11.0
   scipy>=1.7.0
   jupyter>=1.0.0
   ```
   Then run: `pip install -r requirements.txt`

4. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

5. **Open the analysis**
   Navigate to `EDA.ipynb` in your browser and run the cells to see the complete analysis.

## 📈 Key Analysis Areas

### 1. **Data Profiling & Preprocessing**
- Dataset overview and structure analysis
- Missing value identification and treatment
- Data type optimization
- Outlier detection and handling

### 2. **Univariate Analysis**
- Distribution of individual variables
- Summary statistics
- Frequency analysis for categorical variables

### 3. **Bivariate Analysis**
- Survival rate by passenger class
- Gender and survival correlation
- Age distribution and survival patterns
- Fare analysis and survival rates

### 4. **Multivariate Analysis**
- Combined effect of multiple variables
- Interaction between features
- Advanced correlation analysis

### 5. **Feature Engineering**
- Family size calculation (SibSp + Parch)
- Title extraction from names
- Age group categorization
- Fare range binning

## 📊 Key Findings & Insights

### Survival Statistics
- **Overall survival rate**: ~38.4% (342 out of 891 passengers)
- **Gender impact**: Females had a significantly higher survival rate (~74%) compared to males (~19%)
- **Class influence**: 1st class passengers had the highest survival rate (~63%), followed by 2nd class (~47%) and 3rd class (~24%)

### Important Patterns
1. **"Women and children first" policy**: Clear evidence of prioritizing women and children during rescue
2. **Socioeconomic factors**: Higher class passengers had better access to lifeboats
3. **Age factor**: Children (age < 18) had higher survival rates than adults
4. **Family size effect**: Passengers traveling alone or in very large families had lower survival rates

### Missing Data Insights
- **Age**: ~20% missing values (177 passengers)
- **Cabin**: ~77% missing values (687 passengers)  
- **Embarked**: Only 2 missing values

## 🎨 Visualizations

The analysis includes various types of visualizations:

- **Bar Charts**: Survival rates by categorical variables
- **Histograms**: Age and fare distributions
- **Heatmaps**: Correlation matrices and cross-tabulations
- **Box Plots**: Age distribution by survival status
- **Count Plots**: Frequency distributions
- **Violin Plots**: Distribution shapes and densities

## 📝 Methodology

### Data Cleaning Process
1. **Missing Value Treatment**:
   - Age: Filled with median values grouped by passenger class and gender
   - Embarked: Filled with the most frequent port (Southampton)
   - Cabin: Created binary feature indicating cabin information availability

2. **Feature Engineering**:
   - Extracted titles from passenger names (Mr., Mrs., Miss, Master, etc.)
   - Created family size variable
   - Binned continuous variables for better analysis

3. **Outlier Handling**:
   - Identified extreme values in fare and age
   - Applied appropriate treatment strategies

### Statistical Analysis
- Performed chi-square tests for categorical variables
- Calculated correlation coefficients
- Applied t-tests for continuous variables
- Used ANOVA for multiple group comparisons

## 🔍 Data Quality Assessment

### Completeness
- **High quality features**: PassengerId, Survived, Pclass, Name, Sex, SibSp, Parch, Ticket, Fare
- **Medium quality features**: Embarked (99.8% complete)
- **Low quality features**: Age (79.9% complete), Cabin (22.3% complete)

### Consistency
- No duplicate records found
- Consistent data types across features
- Logical relationships maintained (e.g., age ranges, fare values)

## 🚧 Limitations & Considerations

### Dataset Limitations
- **Sample bias**: Dataset represents only 40% of total passengers and crew
- **Missing information**: Significant missing data for cabin and age
- **Historical context**: 1912 social norms and ship safety regulations differ from modern standards

### Analysis Limitations
- **Survival factors**: Analysis focuses on recorded passenger characteristics, not rescue circumstances
- **Causation vs. correlation**: Statistical associations don't imply causation
- **Data imputation**: Filled missing values may introduce bias

## 📚 References & Resources

### Data Source
- [Kaggle Titanic Competition](https://www.kaggle.com/competitions/titanic)
- [Titanic Historical Information](https://www.encyclopedia-titanica.org/)

### Learning Resources
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Seaborn Tutorial](https://seaborn.pydata.org/tutorial.html)
- [Matplotlib User Guide](https://matplotlib.org/stable/users/index.html)

### Inspiration & References
- Kaggle Community Notebooks on Titanic EDA
- "Data Science from Scratch" by Joel Grus
- Various data science blogs and tutorials

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork** the repository
2. **Create** a new branch (`git checkout -b feature/improvement`)
3. **Make** your changes
4. **Commit** your changes (`git commit -am 'Add new analysis'`)
5. **Push** to the branch (`git push origin feature/improvement`)
6. **Create** a Pull Request

### Contribution Ideas
- Add more sophisticated statistical tests
- Implement machine learning models for survival prediction
- Create interactive visualizations
- Improve data preprocessing techniques
- Add cross-validation analysis

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Darshan PC**
- GitHub: [@darshanPC25](https://github.com/darshanPC25)
- Project Link: [https://github.com/darshanPC25/ExploratoryDataAnalysisTitanicDataset](https://github.com/darshanPC25/ExploratoryDataAnalysisTitanicDataset)

## 🏷️ Tags

`data-science` `exploratory-data-analysis` `titanic` `pandas` `python` `jupyter-notebook` `data-visualization` `data-analysis` `machine-learning` `statistics`

## 📅 Project Status

**Status**: Completed ✅
**Last Updated**: July 2025

---

### 💡 Learning Outcomes

By exploring this project, you will gain experience in:
- Python data analysis libraries
- Exploratory data analysis techniques
- Data visualization best practices
- Statistical analysis methods
- Jupyter Notebook development
- Git version control

### 🎓 Educational Value

This project serves as an excellent introduction to:
- **Data Science fundamentals**
- **Statistical thinking**
- **Data storytelling**
- **Python programming for data analysis**
- **Research methodology in data science**

---

*"The good thing about data science is that it doesn't require you to be right all the time. It just requires you to be less wrong than you were yesterday."* - Unknown