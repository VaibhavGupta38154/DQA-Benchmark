# DQA Tool Benchmark Report

## 1. Introduction
**Objective:** Evaluate the performance of the DQA tool against standard benchmarks.

**Scope:** Assess data quality aspects such as completeness, uniqueness, and conformity.

## 2. Data Quality and Stewardship
### Data Quality ✅ Assessment Service ®

**Source:** Volvocars D&A SharePoint

### Three Levels of Data Quality Assessment
🥇 **Level 1 - Data Health Screening (Data Profiling):**
A factual data overview aimed at enabling the creation of data quality rules and delivering a summarized report to aid informed decisions regarding data usage.

🥈 **Level 2 - Data Quality Rule Generation:**
Pre-established fundamental quality assessments that validate typical patterns, formats, and data types.

🥉 **Level 3 - Perform DQ Checks & Generate Report:**
Ensuring data alignment with its intended purpose and use, through the evaluation of Data Quality.

## 3. Benchmarking Methodology
- **Evaluation Metrics:**
  - Completeness (% of missing values handled)
  - Uniqueness (Duplicate detection efficiency)
  - Conformity (Adherence to predefined formats and standards)

### **Tool Capabilities**
- **Supported File Formats:** CSV, JSON, XLSX, PARQUET, XML
- **Supported Data Types:** Structured, Unstructured, Time Series
- **Upload Limit** 200MB per file

## 4. Data Quality Checks for Different Data Types
The DQA tool applies various validation checks to ensure data integrity across different types of files:

### **Structured Data (CSV, XLSX, SQL Databases)**
| Column Type | Applicable Checks |
|-------------|------------------|
| Date | InvalidDateISOFormatCheck, InvalidDateEUFormatCheck, InvalidDateInverseFormatCheck |
| Text | BlankTextCheck, InvalidCharacterFormatCheck, InvalidCategoricalValueCheck |
| Email | InvalidEmailIdFormatCheck |
| Phone Number | InvalidPhoneNumberFormatCheck |
| General | MissingDataCheck, DataDuplicationCheck |
| Conformity | Ensuring adherence to predefined data formats |

### **Unstructured Data (JSON, XML, Free Text)**
| Data Aspect | Applicable Checks |
|------------|------------------|
| Key-Value Pairs | MissingDataCheck, DataDuplicationCheck, InvalidCharacterFormatCheck |
| Embedded Dates | InvalidDateISOFormatCheck, InvalidDateInverseFormatCheck |
| Free Text Fields | BlankTextCheck, InvalidCategoricalValueCheck |
| Email & Phone | InvalidEmailIdFormatCheck, InvalidPhoneNumberFormatCheck |
| Conformity | Adherence to expected schema and structure |

### **Time Series Data**
| Data Aspect | Applicable Checks |
|------------|------------------|
| Timestamps | InvalidDateISOFormatCheck, InvalidDateInverseFormatCheck |
| Sequential Data | MissingDataCheck, DataDuplicationCheck |
| Value Consistency | InvalidCategoricalValueCheck |
| Conformity | Ensuring proper time-series format adherence |

## 5. Most Common Issues in the Dataset
The following issues were frequently identified across different datasets:
- **Missing Data**: Incomplete records affecting analysis quality
- **Duplicate Entries**: Redundant data points inflating dataset size
- **Invalid Formatting**: Data entries not conforming to expected formats (dates, emails, phone numbers, etc.)
- **Schema Violations**: Structural inconsistencies in unstructured datasets

## 6. Column-wise Error Statistics
The DQA tool provides detailed statistics for errors found in each column of a dataset, including:
- **Total records checked**
- **Percentage of errors detected**
- **Most frequent issue per column**

## 7. Alerts & Notifications
The tool generates alerts based on predefined thresholds for:
- High levels of missing or duplicate data
- Violations of formatting rules
- Schema inconsistencies in unstructured data

