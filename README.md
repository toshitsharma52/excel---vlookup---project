# excel---vlookup---project
# IPL Team Ratings Aggregator – Excel VLOOKUP Project

## Overview

This Excel project consolidates individual team ratings (Batting, Bowling, Fielding) from three different judges into a single **Main Sheet** using the `VLOOKUP` function. It demonstrates how to:

- Organize data across multiple sheets
- Use `VLOOKUP` with exact matching (`FALSE`)
- Avoid common lookup errors by correctly scoping table arrays

## File Structure

The Excel file `mini project_Vlookup_practice.xlsx` contains four sheets:

1. **Judge 1** – Ratings given by Judge 1 (all 5’s)
2. **Judge 2** – Ratings given by Judge 2 (all 1’s)
3. **Judge 3** – Mixed ratings (5,4,3,2,1)
4. **Main Sheet** – Consolidates data from Judge 1, Judge 2, and Judge 3 using VLOOKUP

## How It Works

### Judge Sheets

Each judge sheet has the same structure:

| Team Name | Batting | Bowling | Fielding |
|-----------|---------|---------|----------|
| CSK       | 5       | 5       | 5        |
| RCB       | 5       | 5       | 5        |
| ...       | ...     | ...     | ...      |

(Mixed values in Judge 3)

### Main Sheet Layout

The Main Sheet brings all judge scores together side by side:

| Team Name | Judge1 Batting | Judge1 Bowling | Judge1 Fielding | Judge2 Batting | ... | Judge3 Fielding |
|-----------|----------------|----------------|------------------|----------------|-----|------------------|

Each cell contains a `VLOOKUP` formula that references the corresponding judge sheet.

## Formula Example

For **CSK's Judge 1 Batting**:

```excel
=VLOOKUP(A3,'Judge 1'!A1:D12,2,FALSE)
