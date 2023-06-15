# Data Warehousing, BI and Dimensional Modeling Primer
## Introduction
### Fact Tables for Measurement
- The fact table in a dimensional model stores the performance measurements resulting
from an organization’s business process events
- The term fact represents a business measure
- Each row in a fact table corresponds to a measurement event
- The data on each row is at a specifi c level of detail, referred to as the grain
- A true text fact is rare because the unpredictable content of a text fact, like a freeform text comment, makes it nearly impossible to analyze (not so true anymore in modern times)
- Fact tables tend to be deep in terms of the number of rows, but narrow in terms of the number of columns
- there are three types of fact tables:
    - `transaction`
    - `periodic snapshot`
    - `accumulating snapshot`

    - all fact tables have two or more foreign keys that connect to the dimensions primary keys
    - fact tables generally also have their own primary key composed of a subset of the foreign keys --> often called composite key

###  Dimension Tables for Descriptive Context
- The dimension tables contain the textual context associated with a business process measurement event
- It is not uncommon for a dimension table to have 50 to 100 attributes
- Dimension attributes serve as the primary source of query constraints, groupings, and report labels
- dimension tables typically are highly denormalized with fl attened many-to-one relationships within a single dimension table