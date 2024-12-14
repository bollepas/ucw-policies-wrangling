# ucw-policies-wrangling
## Data Wrangling

### Project Description
Data Wrangling of UCW’s Substance Use Policy for Structured Analysis

### Project Title
Data Wrangling for UCW’s Substance Use Policy Insights

### Objective
To clean, transform, and consolidate policy details for structured analysis and reporting.

### Dataset
The dataset includes:
- Full policy text
- Related policy references and associated procedures
- Legislative references impacting policy implementation

### Methodology
#### 1. Data Ingestion
- Raw policy data was uploaded to an Amazon S3 bucket (`policy-raw-ucw`) for centralized management.
- AWS KMS encryption was applied for security compliance.

#### 2. Data Profiling and Cleaning
- AWS Glue DataBrew profiled the policy text, identifying:
  - Inconsistent formatting
  - Redundant information
  - Key data points (e.g., definitions, responsibilities, and procedures)
- Cleaning steps included:
  - Standardizing headings and sections
  - Removing irrelevant metadata

#### 3. Data Transformation
- AWS Glue ETL automated the transformation process:
  - Segmented data into categories like "Definitions," "Responsibilities," and "Legislative Scope."
  - Standardized schema to ensure compatibility with analytical tools.
  - Created structured outputs in JSON and Parquet formats for querying.

#### 4. Data Consolidation
- Final datasets were stored in S3 buckets (`policy-trf-ucw`) with folders organized by content categories.

### Tools and Technologies
- **AWS Services:** S3, Glue DataBrew, Glue ETL for profiling, cleaning, and transformation.
- **Data Storage:** JSON and Parquet formats in AWS S3 for efficient querying.
- **Data Querying:** Amazon Athena for structured data exploration.

### Deliverables
- Cleaned and transformed policy dataset stored in AWS S3.
- Structured outputs for further analysis and visualization.
- Documentation of the wrangling process for reproducibility.

### Conclusion
Data wrangling transformed the UCW Substance Use Policy into a structured and queryable format, ensuring readiness for downstream analysis. By using AWS services, the process was efficient, secure, and scalable for future policy analysis projects.
