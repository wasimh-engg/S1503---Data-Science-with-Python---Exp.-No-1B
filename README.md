# Experiment 1.B : Product Price Analysis Using Python Functions

## Aim
To analyze quarterly product sales data across multiple products and quarters using 2D NumPy arrays and Python statistical functions.

## Algorithm

1. **Start** the program.
2. **Import Library**: Import the `numpy` module as `np` for numerical array operations.
3. **Initialize 2D Sales Matrix**: Create a $3 \times 4$ NumPy array `sales` containing quarterly sales figures for 3 products across 4 quarters.
4. **Compute Product-Wise Totals**: Calculate the sum of sales across columns (`axis=1`) for each product using `np.sum(sales, axis=1)`.
5. **Compute Quarter-Wise Totals**: Calculate the sum of sales across rows (`axis=0`) for each quarter using `np.sum(sales, axis=0)`.
6. **Compute Overall Statistical Metrics**:
   * Calculate the overall mean sales across all entries using `np.mean(sales)`.
   * Identify the maximum sales figure using `np.max(sales)`.
   * Identify the minimum sales figure using `np.min(sales)`.
7. **Display Analysis Summary**: Print the original sales matrix, product-wise totals, quarter-wise totals, overall average, highest sale, and lowest sale.
8. **Stop** the program.
## Program

```python
import numpy as np

sales = np.array([
    [1000, 1200, 1150, 1400],
    [800, 950, 1050, 1300],
    [1500, 1600, 1550, 1700]
])

print("Sales Data (Rows=Products, Columns=Quarters):\n", sales)

product_total = np.sum(sales, axis=1)
quarter_total = np.sum(sales, axis=0)
overall_avg = np.mean(sales)

print("\nTotal Sales per Product:", product_total)
print("Total Sales per Quarter:", quarter_total)
print("Overall Average Sales:", overall_avg)
print("Highest Sale:", np.max(sales))
print("Lowest Sale:", np.min(sales))
```

## Output
```text
Sales Data (Rows=Products, Columns=Quarters):
[[1000 1200 1150 1400]
 [ 800  950 1050 1300]
 [1500 1600 1550 1700]]

Total Sales per Product: [4750 4100 6350]
Total Sales per Quarter: [3300 3750 3750 4400]
Overall Average Sales: 1266.6666666666667
Highest Sale: 1700
Lowest Sale: 800
```

## Result

The program successfully analyzes quarterly product sales using 2D NumPy arrays and Python statistical aggregation functions.
