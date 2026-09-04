# Hands-On-10B-python-nested-while-loops

# Lesson 10 B: Python Nested while Loops

## Executive Summary
This project explores multi-dimensional iteration and nested flow control in Python using `while` loops. Through hands-on scenarios—including e-commerce product permutation generators, banking transaction risk evaluations, and hospital appointment scheduling matrices—this repository illustrates how nested conditional loops systematically iterate over multi-dimensional datasets to build combinatorial matrices, flag risk exceptions, and generate incremental entity identifiers.

---

## Project Background & Problem Statement
Data processing pipelines frequently require evaluation across multiple dependent dimensions—such as paired product attributes, customer-to-transaction mappings, or schedule-to-time-slot matrix generation.

Without structured nested `while` iteration:
* **Product Catalog Generation:** E-commerce systems struggle to generate Cartesian product variations across attributes (e.g., combining every product size with every color variant).
* **Cross-Dimensional Risk Auditing:** Financial engines risk bypassing transaction anomaly checks when iterating across multiple customer accounts without persistent state resets.
* **Matrix & Slot Scheduling:** Healthcare and operational scheduling systems fail to map dynamic resource availability across multi-time-slot windows while tracking incremental appointment IDs.

This project addresses these needs by constructing nested `while` loop architectures that manage outer and inner loop counter resets, compute cross-dimensional iterations, and track running metrics across multi-tiered data structures.

---

## Real-World Business & Operational Impact

* **E-Commerce Product Permutations:** Automates the generation of stock-keeping unit (SKU) combinations across product sizes and color variations, providing total product variation counts for inventory management.
* **FinTech & Banking Audit Systems:** Evaluates cross-customer transaction sets against risk thresholds, auditing each transaction, flagging high-value transactions exceeding threshold limits (e.g., transactions over $100,000), and recording total audit comparisons.
* **Healthcare Operations & Appointment Matrix:** Generates complete matrix schedules pairing available medical staff with daily time slots, assigning sequential appointment IDs for booking systems.

---

## Tools & Technical Environment

* **Core Language:** Python 3.x
* **Development Environment:** Jupyter Notebook / JupyterLab
* **Core Loop Features & Concepts Applied:**
* **Nested Iteration:** Outer `while i < len(...)` and inner `while j < len(...)` loop evaluation
* **State Resetting:** Re-initializing inner index variables (`j = 0`) at the start of each outer loop execution
* **Counter & Identifier Tracking:** Stateful accumulation (`total_variations = len(sizes) * len(colors)`, `review_count += 1`, `total_comparisons += 1`, `total_appointments += 1`, `appointment_id += 1`)
* **Conditional Threshold Auditing:** Multi-variable evaluation (`if transactions[j] > risk_threshold:`)

---

## Technical Capabilities & Concepts Mastered

* **Multi-Dimensional State Control:** Mastered the structure of nested `while` loops by explicitly maintaining and incrementing primary (`i`) and secondary (`j`) loop index pointers.
* **Inner Counter Re-Initialization:** Enforced proper state re-initialization by resetting the inner loop counter (`j = 0`) prior to executing each inner cycle.
* **Exception & Risk Auditing:** Constructed logic to iterate across paired list structures and flag items meeting risk threshold criteria.
* **Sequential Matrix Generation:** Implemented incremental state counters (`appointment_id += 1`) across nested loops to construct auto-incrementing schedule tables.

---

## Detailed Exercise Breakdown

### Exercise 1: E-Commerce Product Combination Generator
* Generated combinations across available product sizes (`"Small"`, `"Medium"`, `"Large"`) and colors (`"Black"`, `"White"`, `"Blue"`).
* Reset the color index (`j = 0`) inside the outer loop to cycle through every color variant for each product size.
* Computed total variation count dynamically (`total_variations = len(sizes) * len(colors)`), outputting 9 product variations.

### Exercise 2: Banking Transaction Risk Audit System
* Audited transaction records (`[45000, 125000, 75000]`) across customer identifiers (`["C001", "C002", "C003"]`) against a risk threshold of `$100,000`.
* Standard Implementation: Iterated through all transactions for each customer and logged transactions exceeding the threshold.
* Additional Challenge: Added state tracking variables (`review_count`, `total_comparisons`) to record flagged transactions (3) and total comparison checks performed (9).

### Exercise 3: Hospital Appointment Scheduling Matrix
* Constructed an operational scheduling matrix pairing doctors (`"Dr. Ahmed"`, `"Dr. Grace"`, `"Dr. Michael"`) with available time slots (`"9:00 AM"`, `"11:00 AM"`, `"2:00 PM"`, `"4:00 PM"`).
* Standard Implementation: Formatted and printed doctor slot groupings separated by blank lines.
* Additional Challenge: Introduced `total_appointments` counter to calculate total available scheduling slots (12).
* Expert Challenge: Integrated an auto-incrementing `appointment_id` counter starting at 1, assigning a unique identifier to each generated slot.

---

## Key Output Artifacts

```text
--- EXERCISE 1 OUTPUT ---
Small - Black
Small - White
Small - Blue

Medium - Black
Medium - White
Medium - Blue

Large - Black
Large - White
Large - Blue

Total Product Variations: 9


--- EXERCISE 2 (STANDARD) OUTPUT ---
Customer: ['C001', 'C002', 'C003'][i] | Transaction: [45000, 125000, 75000][j] | Status REVIEW
Customer: ['C001', 'C002', 'C003'][i] | Transaction: [45000, 125000, 75000][j] | Status REVIEW
Customer: ['C001', 'C002', 'C003'][i] | Transaction: [45000, 125000, 75000][j] | Status REVIEW


--- EXERCISE 2 (ADDITIONAL CHALLENGE) OUTPUT ---
Customer: C001 | Transaction: 125000 | Status REVIEW
Customer: C002 | Transaction: 125000 | Status REVIEW
Customer: C003 | Transaction: 125000 | Status REVIEW
Transactions Requiring Review: 3
Total Comparisons Performed: 9


--- EXERCISE 3 (STANDARD) OUTPUT ---
Dr. Ahmed - 9:00 AM
Dr. Ahmed - 11:00 AM
Dr. Ahmed - 2:00 PM
Dr. Ahmed - 4:00 PM

Dr. Grace - 9:00 AM
Dr. Grace - 11:00 AM
Dr. Grace - 2:00 PM
Dr. Grace - 4:00 PM

Dr. Michael - 9:00 AM
Dr. Michael - 11:00 AM
Dr. Michael - 2:00 PM
Dr. Michael - 4:00 PM


--- EXERCISE 3 (ADDITIONAL CHALLENGE) OUTPUT ---
Dr. Ahmed - 9:00 AM
Dr. Ahmed - 11:00 AM
Dr. Ahmed - 2:00 PM
Dr. Ahmed - 4:00 PM

Dr. Grace - 9:00 AM
Dr. Grace - 11:00 AM
Dr. Grace - 2:00 PM
Dr. Grace - 4:00 PM

Dr. Michael - 9:00 AM
Dr. Michael - 11:00 AM
Dr. Michael - 2:00 PM
Dr. Michael - 4:00 PM

Total Possible Appointments: 12


--- EXERCISE 3 (EXPERT CHALLENGE) OUTPUT ---
Appoinment 1: Dr. Ahmed - 9:00 AM
Appoinment 2: Dr. Ahmed - 11:00 AM
Appoinment 3: Dr. Ahmed - 2:00 PM
Appoinment 4: Dr. Ahmed - 4:00 PM

Appoinment 5: Dr. Grace - 9:00 AM
Appoinment 6: Dr. Grace - 11:00 AM
Appoinment 7: Dr. Grace - 2:00 PM
Appoinment 8: Dr. Grace - 4:00 PM

Appoinment 9: Dr. Michael - 9:00 AM
Appoinment 10: Dr. Michael - 11:00 AM
Appoinment 11: Dr. Michael - 2:00 PM
Appoinment 12: Dr. Michael - 4:00 PM

Total Possible Appointments: 12

```

## Author: Muhyideen Saadah
