# Beginning-DAX-Seamark-Errata
Personal Errata for Phil Seamark's "Beginning DAX with Power BI" 1/e [book](https://doi.org/10.1007/978-1-4842-3477-8) published by Apress

<img src="Images/Seamark - Beginning DAX Book.png" alt="Phil Seamark's beginning DAX book cover" width="200">

## Chapter 5 (Joins)

### p. 98 - Table 5.2

| Make | Model | Year | Index |
| --- | --- | --- | --- |
| Toyota | Corolla | 2018 | 100 |
| Toyota | Corolla | ***2019*** | 200 |
| Hyundai | Elantra | ***2018*** | 300 |
| Hyundai | Elantra | 2019 | 400 |
| Ford | Focus | 2018 | 500 |
| Ford | Focus | 2019 | 600 |

## Chapter 6 (Filtering)

### p. 133 - Listing 6-1

*Should be >= 10, rather than > 10*
```dax
Count of Sales (10 or more) =
COUNTROWS (
    FILTER (
        'Fact Sale',
        'Face Sale'[Quantity] >= 10
    )
)
```
