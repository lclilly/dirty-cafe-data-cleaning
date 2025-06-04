# dirty-cafe-data-cleaning
Cleaning Café Sales Data Using Power Query
Opened Excel> Data> Get Data > From Text/CSV > Transfrom Data
Use the first row as a header.
Change quantity from text(abc), to whole number(123), price per unit and total spent from text to decimal number, and transaction date from text to date.
In item, payment method, and location columns, replace blank, unknown, and error values as follows. Item = Item Not Recorded. Payment Method = Unknown. Location = Unspecified.
Add a custom column calculated_total = price_per_unit*quantity to get the null values in total_spent column
Add a conditional column, final_total_spent = if total_spent is null, then output value from calculated_total, else output value from total_spent
Remove calculated_total and original total_spent columns and rename final_total_spent to total_spent
Check for negatives in the total_spent column
Load and save as cleaned_cafe_data
