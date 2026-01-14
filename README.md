# French Gas Price Prediction with Apache Spark ML

A comprehensive machine learning project analyzing and predicting gas prices across France (2022-2024) using Apache Spark and PySpark ML. This project processes over 12 million records to forecast fuel prices using both Linear Regression and Random Forest models.

## 📊 Project Overview

This project demonstrates end-to-end data science workflow including:
- Large-scale data processing with Apache Spark
- Feature engineering and time series analysis
- Multiple ML model development and comparison
- Geographic visualization with interactive maps
- Statistical analysis and model interpretation

## 📁 Project Structure

```
.
├── Spark_project.ipynb          # Main analysis notebook
├── gas_prices_config.yaml       # Configuration file
├── README.md                    # Project documentation
├── gas_price_data/              # Downloaded data files (not in repo)
├── plots/                       # Generated visualizations
│   ├── gas_price_trends.png
│   ├── linear_regression_errors.png
│   ├── random_forest_errors.png
│   └── model_comparison_facetgrid.png
└── maps/                        # Interactive maps
    ├── map_Gazole.html
    ├── map_SP95.html
    ├── map_SP98.html
    └── map_E10.html
```

## 📈 Dataset

- **Source**: French gas price database (2022-2024)
- **Size**: 12+ million records
- **Fuel Types**: Gazole (Diesel), SP95, SP98, E10
- **Features**: Date, location (lat/lon, department), station type, fuel type, price
- **Temporal Coverage**: 156 weeks across 3 years

### Data Sources
- Gas price data: Historical daily prices from French gas stations
- Geographic data: French department boundaries (GeoJSON)
- Station information: Location and service data

## 🛠️ Technologies Used

- **Apache Spark 3.5.0** - Distributed data processing
- **PySpark ML** - Machine learning pipelines
- **Python 3.x** - Core programming language
- **Libraries**:
  - `pyspark.sql` - DataFrame operations
  - `pyspark.ml` - Machine learning algorithms
  - `pandas` - Data manipulation
  - `matplotlib` & `seaborn` - Visualization
  - `folium` - Interactive mapping
  - `geopandas` - Geographic data handling
  - `pyyaml` - Configuration management

## 🚀 Getting Started

### Prerequisites

```bash
# Java 11 or 17 (required for Spark)
java -version

# Python 3.8+
python --version
```

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/jevdende/Spark.git
cd Spark
```

2. **Install dependencies**
```bash
pip install pyspark pandas matplotlib seaborn folium geopandas pyyaml requests
```

3. **Configure Java Home**
```bash
export JAVA_HOME=/usr/lib/jvm/java-1.17.0-openjdk-amd64
```

### Running the Project

1. **Open the notebook**
```bash
jupyter notebook Spark_project.ipynb
```

2. **Execute cells sequentially**
   - The notebook is divided into 4 main sections:
     - 0. Imports and PySpark setup
     - 1. Data collection
     - 2. Data preprocessing
     - 3. Data visualization
     - 4. Modeling

3. **Configuration**
   - Modify `gas_prices_config.yaml` to change:
     - Data download years
     - Directory paths
     - Data source URL

## 👤 Author

**Jesse van der Ende**
- ENSAI Student
- Course: IT Tools 2 - Spark
