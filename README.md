# 📈 Probability Density Function Estimation using NO₂ Data

## Project Objective

This assignment focuses on modeling the probability distribution of air pollution data using a non-linear transformation and curve fitting approach.

The goal is to:

- Extract NO₂ values from an air quality dataset
- Apply a roll-number-based transformation
- Estimate parameters of a custom probability density function
- Compare empirical and fitted distributions visually

---

## Dataset

The dataset used contains air quality measurements across India.

Feature used:
- `no2` (Nitrogen Dioxide concentration)

Missing values are removed before performing calculations.

---

## Mathematical Formulation

### Step 1: Data Transformation

Let:

x = NO₂ values  

The transformed variable is:

z = x + a sin(bx)

Where:

a = 0.05 × (r mod 7)  
b = 0.3 × ((r mod 5) + 1)

For roll number 102303139:

- r % 7 = 1  
- r % 5 = 4  

Therefore:

a = 0.05  
b = 1.5  

---

### Step 2: Probability Density Model

The fitted probability density function is:

p̂(z) = c e^(−λ (z − μ)²)

Where:

λ controls the spread  
μ represents the mean  
c is the scaling constant  



## Implementation Workflow

1. Load dataset using pandas
2. Extract `no2` column
3. Remove null values
4. Compute constants a and b
5. Apply transformation to obtain z
6. Generate histogram (empirical PDF)
7. Fit exponential-quadratic model
8. Plot histogram and fitted curve

---

## Libraries Used

Install dependencies before running:

```bash
pip install pandas numpy matplotlib scipy
```

Used packages:

- pandas
- numpy
- matplotlib
- scipy.optimize

---

## How to Run

### Option 1: Using Python Script

```bash
python advancemathematics (1).py
```

### Option 2: Using Jupyter Notebook

```bash
jupyter notebook AdvanceMathematics (1).ipynb
```

Run all cells sequentially.

---

## Output

The program prints:

```
a = 0.05
b = 1.5

Lambda = <estimated_value>
Mu = <estimated_value>
c = <estimated_value>
```

It also generates:

- Histogram of transformed data
- Fitted probability density curve

The plot visually confirms how well the model fits the data.

---

## Graph Interpretation

- Blue bars → Empirical PDF (actual distribution)
- Orange curve → Fitted model
- Close alignment indicates good parameter estimation

Minor mismatch may occur due to skewness in pollution data.

---

## Key Concepts Demonstrated

- Non-linear transformation
- Data normalization
- Histogram-based density estimation
- Non-linear curve fitting
- Gaussian-like probability modeling

---

## Academic Context

Course:Predictive Analytics using Statistics 
Assignment:Learn Probability Density Functions using Roll-Number-Parameterized Non-Linear Model.

This project demonstrates practical implementation of probability theory concepts on real environmental data.

---

## Author

Krish Mahajan  
Roll Number: 102303139  

---
