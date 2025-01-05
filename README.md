# Ultramarathon Data Analysis

This project focuses on analyzing a dataset containing two centuries of ultramarathon (UM) race data. It filters, cleans, and visualizes key insights about races held in the USA in 2020 with a focus on 50km and 50mi events. The dataset contains approximately 7.46 million rows, providing a comprehensive view of ultramarathon events and participants.

---

## Dataset

### Source
- The dataset is named `TWO_CENTURIES_OF_UM_RACES.csv`.

### Features
Key columns in the dataset include:
- **Year of event**: The year the race occurred.
- **Event name**: Name of the race.
- **Event distance/length**: Distance categories (e.g., 50k, 50mi).
- **Athlete ID**: Unique identifier for participants.
- **Athlete gender**: Gender of the participant.
- **Athlete age category**: Age group.
- **Athlete performance**: Performance metrics.
- **Athlete average speed**: Average speed during the event.

---

## Objectives
1. Filter data for:
   - USA-based races.
   - 50km or 50mi race lengths.
   - Events occurring in 2020.
2. Clean and preprocess the dataset:
   - Handle missing values and duplicates.
   - Extract and format relevant details from columns.
   - Calculate athlete age using event year and birth year.
3. Visualize key insights:
   - Compare performance by gender and distance.
   - Identify top-performing age groups for 50mi races.
   - Examine athlete average speed trends by age and gender.

---

## Data Cleaning Steps

1. **Filter Relevant Data**:
   - Use `.isin()` to select 50km and 50mi distances.
   - Extract USA-based events using string parsing on `Event name`.
2. **Transform Columns**:
   - Calculate athlete age using: `age = Year of event - Athlete year of birth`.
   - Remove irrelevant columns like `Athlete club`, `Athlete country`, and others.
3. **Handle Missing and Duplicate Values**:
   - Drop rows with null values.
   - Remove duplicate entries.
4. **Rename Columns**:
   - Standardize column names for consistency and clarity (e.g., `Year of event` -> `year`).

---

## Visualizations

1. **Race Length Comparison**:
   - Histogram comparing participation in 50km vs. 50mi races.
2. **Performance by Gender**:
   - Violin plot showing gender-wise distribution of average speed.
3. **Age vs. Speed**:
   - Scatter plot analyzing the relationship between age and average speed.

---

## Key Findings

1. **Performance Differences**:
   - Observed speed differences between male and female participants in 50km and 50mi races.
2. **Top Age Groups**:
   - Identified the best-performing age groups for 50mi races with a minimum of 20 participants.
3. **Participation Trends**:
   - Insights into participation trends by distance and gender.

---

## How to Use

1. **Clone the Repository**:
   ```bash
   git clone <repository-link>
   ```
2. **Install Dependencies**:
   - Python libraries: Pandas, Seaborn.
   ```bash
   pip install pandas seaborn
   ```
3. **Run the Analysis**:
   - Open and execute the provided Python script in a Jupyter Notebook or your preferred IDE.

---

## Questions Addressed

1. What are the differences in average speed in 50km and 50mi races?
   ![img](https://github.com/SriSurya-DA/Marathon_Analysis_Two_Centuries/blob/main/Avg%20seed%20for%2050mils.png)
   ![img](https://github.com/SriSurya-DA/Marathon_Analysis_Two_Centuries/blob/main/Avg%20speed%20for%2050KM.png)
   
2. Which age groups perform best in 50mi races with significant participation in both(50KM and 50mils)?
   ![img](https://github.com/SriSurya-DA/Marathon_Analysis_Two_Centuries/blob/main/avgspeed%20for%20male%26female%20in%20both%20sets.png)

3. How does average speed vary by age and gender?
   ![img](https://github.com/SriSurya-DA/Marathon_Analysis_Two_Centuries/blob/main/avg%20speed%20Vs%20gender.png)


