# Probability Density Function Learning

## Objective

- The objective of this project is to determine the parameters (λ, μ, c) of a probability density model after applying a customized non-linear transformation based on the university roll number to NO₂ data.
---

## Methodology

### Step 1: Data Preparation
- Loaded dataset in Google Colab.
- Selected `no2` feature.
- Removed missing values.
- Converted data to NumPy array.

### Step 2: Apply Transformation

Transformation:

z = x + aᵣ sin(bᵣ x)

Where:

aᵣ = 0.05 × (r mod 7)  
bᵣ = 0.3 × (r mod 5 + 1)  

Roll Number: **102303061**

Computed:

r mod 7 = 0 → aᵣ = 0.0  
r mod 5 = 1 → bᵣ = 0.6  

Final transformation:

z = x  

---

### Step 3: Parameter Estimation

Model:

p̂(z) = c e^(−λ (z − μ)²)

Using Maximum Likelihood Estimation:

μ = mean(z)  
variance = var(z)  
λ = 1 / (2 × variance)  
c = 1 / √(2π × variance)  

---

## Final Results

μ = 25.809622897811263  
λ = 0.001460436525489001  
c = 0.021560876239314915  
