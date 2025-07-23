
# Excel: INDEX-MATCH vs VLOOKUP

This project demonstrates how to use `INDEX-MATCH` and `VLOOKUP` functions in Excel to retrieve specific values based on a StockCode (e.g., quantity sold). It's part of my Excel practice for data analysis.

---

## 📌 What does it solve?

You have two tables:
- One table contains `StockCode` and sales data (`Quantity`)
- The other table needs to **look up** how many units were sold for a given StockCode

---

## 🧮 1. INDEX-MATCH Method

This is a two-step lookup:

```excel
=INDEX(range_to_return_value, MATCH(lookup_value, range_to_search, 0))
```
```excel
=INDEX(D:D, MATCH(G3, A:A, 0))
```

G3: StockCode we want to look up (e.g., 21730)

A:A: Column where we search for the StockCode

D:D: Quantity values we want to return

```excel
=VLOOKUP(lookup_value, table_array, column_index, FALSE)
=VLOOKUP(F3, A:D, 4, FALSE)
```
F3: StockCode to search

A:D: The full table

4: Column number in the table where the value to return is found (Quantity)

FALSE: Ensures exact match
