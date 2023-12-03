# 208Dowels 📊

Welcome to **208dowels**.

This project is centered around statistical analysis using the chi-squared (χ²) test to validate the quality control of mass-produced dowels.

## Language and Tools 🛠️

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

- **Language:** Python
- **Compilation:** Via Makefile, including `re`, `clean`, and `fclean` rules.
- **Binary Name:** 208dowels

## Project Overview 🔎

The goal of 208dowels is to analyze the quality of dowels produced by a power hammer.

The program takes the observed serial of defective pieces and computes statistical fits using binomial distribution. It validates the fits using the χ² test, considering the constraints of statistical classes and degrees of freedom.

### Key Features

- **χ² Test Analysis:** Perform statistical fits and validate them using the χ² test.
- **Statistical Classes Merging:** Aggregate smaller classes to meet minimum size criteria.
- **Comprehensive Output:** Display observed and theoretical sizes for each statistical class, the probability distribution, the χ² value, degrees of freedom, and fit validity.

### Usage

```
∼> ./208dowels -h
USAGE
    ./208dowels O0 O1 O2 O3 O4 O5 O6 O7 O8
DESCRIPTION
    Oi   size of the observed class
```

### Exemples

```
∼/B-MAT-400> ./208dowels 6 4 10 18 20 19 11 5 7
x   | 0-1   | 2     | 3     | 4     | 5     | 6     | 7+    | Total
Ox  | 10    | 10    | 18    | 20    | 19    | 11    | 12    | 100
Tx  | 8.0   | 13.8  | 19.2  | 19.9  | 16.3  | 11.1  | 11.7  | 100
Distribution:           B(100, 0.0410)
Chi-squared:            2.029
Degrees of freedom:     5
Fit validity:           80% < P < 90%

∼/B-MAT-400> ./208dowels 6 4 10 8 20 19 11 5 17
x   | 0-1   | 2-3   | 4     | 5     | 6-7   | 8+    | Total
Ox  | 10    | 18    | 20    | 19    | 16    | 17    | 100
Tx  | 5.2   | 26.7  | 19.1  | 17.7  | 22.2  | 9.0   | 100
Distribution:           B(100, 0.0460)
Chi-squared:            16.119
Degrees of freedom:     4
Fit validity:           P < 1%
```

## Installation and Usage 💾

1. Clone the repository.
2. Compile the program using the provided Makefile.
3. Run the program: `./208dowels O0 O1 O2 O3 O4 O5 O6 O7 O8`.
4. For detailed guidelines, refer to `208dowels.pdf`.

## License ⚖️

This project is released under the MIT License. See `LICENSE` for more details.
