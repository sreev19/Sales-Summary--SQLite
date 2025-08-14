##  Basic Sales Summary using Python & SQLite

### Objective
Fetch and visualize simple sales summary (total quantity sold & total revenue) from a SQLite database using Python.

### Steps
1. **Create/Connect** to `sales_data.db` using `sqlite3`.
2. **Create & insert** sample data into a `sales` table.
3. **Run SQL Query** to calculate:
   - `SUM(quantity)` → Total Quantity Sold
   - `SUM(quantity * price)` → Revenue
4. **Load results** into Pandas DataFrame.
5. **Display output** with `print()` and plot a bar chart using `matplotlib`.

### Example SQL
```sql
SELECT product, 
       SUM(quantity) AS total_qty, 
       SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;
