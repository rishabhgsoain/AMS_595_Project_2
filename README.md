# Project Overview

This project computes and visualizes the **boundary of the Mandelbrot fractal** and approximates it using **polynomial fitting and numerical integration**.

The work involves generating complex points, identifying the boundary between interior and exterior regions, fitting a polynomial curve to that boundary, and calculating the curve length via integration.

The project consists of the following main tasks:

---

### **Task 1: Fractal Function Implementation**

- Implements the `fractal()` function that determines whether a given complex number `c` belongs to the Mandelbrot set.  
- Uses an iterative rule:  
  \[
  z_{n+1} = z_n^2 + c
  \]
- Returns the iteration count until divergence (or 0 if the point stays inside the set).

---

### **Task 2: Boundary Detection Using Bisection**

- Defines the `indicator_fn_at_x()` function to check whether a point along a vertical line at a fixed `x` is inside or outside the fractal.  
- Implements the `bisection()` method to locate the **exact boundary point** where the transition occurs from inside to outside.  
- Samples **10³ (1000)** points across the x-axis to build the fractal boundary dataset.

---

### **Task 3: Polynomial Fitting and Visualization**

- Fits a **15th-degree polynomial** using MATLAB’s `polyfit()` on the computed boundary points.  
- Plots the results:
  - Blue dots → boundary points
  - Red line → polynomial fit approximation  
- Produces a smooth visual curve that closely follows the fractal’s edge.

---

### **Task 4: Curve Length Calculation via Integration**

- Defines `poly_len()` to compute the arc length of the fitted polynomial using:
  \[
  L = \int_a^b \sqrt{1 + (dy/dx)^2} \, dx
  \]
- Uses MATLAB’s built-in `integral()` function for numerical evaluation.  
- Performs **two tests**:
  - A degree-5 quick check for comparison.  
  - A degree-15 full computation for the final curve length.


## Requirements

- **MATLAB R2021a or later** (Octave compatible with `quad()` for integration).  
- No external toolboxes required.  
- Plots and figures generated using MATLAB’s built-in plotting functions.

---

## Files

| File | Description |
|------|--------------|
| `fractal_boundary_fit.m` | Main script containing all functions (`fractal`, `indicator_fn_at_x`, `bisection`, `poly_len`). |
| `report.tex` | LaTeX report describing work done, results, and discussion (max 500 words). |
| `fractal_plot.png` | Visualization of the fractal boundary (blue) and polynomial fit (red). |

---

## Author

**Rishabh Gosain**  
