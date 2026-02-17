# Assignment-1: Learning Probability Density Functions

**Course:** Probability / Data Analysis  
**Objective:**  
To transform NO₂ air-quality data using a roll-number-parameterized nonlinear function and estimate the parameters of a Gaussian-type probability density function from the transformed variable.

---

## Description 

This assignment applies a roll-number-based nonlinear transformation to NO₂ air-quality data, estimates Gaussian PDF parameters from the transformed variable, and demonstrates data preprocessing, statistical modeling, and reproducible analysis using Python and NumPy.

---

## Dataset

- **Source:** Kaggle India Air Quality Dataset  
- **Feature Used:** NO₂ concentration values  
- Missing values are removed before analysis.

---

## Methodology

### Step-1: Nonlinear Transformation

Each NO₂ value x is transformed into:


z = x + a_r sin(b_r x)


where:


a_r = 0.05(r bmod 7), quad
b_r = 0.3(r bmod 5 + 1)


For roll number **102303554**:

- (a_r = 0.15)  
- (b_r = 1.5)

---

### Step-2: PDF Parameter Estimation

The probability density function:

{p}(z) = c , e^{-lambda (z-mu)^2}


Parameters are estimated as:

- **Mean:** ( mu = text{mean}(z) )  
- **Variance:** ( sigma^2 = text{var}(z) )  
- **Lambda:** ( lambda = frac{1}{2 sigma^2}
- **Constant:**  c = sqrt{frac{lambda}{pi}} 

---

## Implementation Tools

- Python  
- Pandas  
- NumPy  

Used for:

- Data preprocessing  
- Nonlinear transformation  
- Statistical estimation  

---

## Output

Final submission includes the learned parameters:


- mu = 25.814687284943872
- lambda = 0.0014612298133120176
- c = 0.021566731221112533


These represent the Gaussian PDF parameters of the transformed NO₂ variable.

---

## Learning Outcomes

- Nonlinear feature transformation  
- Probability density estimation  
- Statistical parameter learning  
- Reproducible data analysis using Python
