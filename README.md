import pandas as pd

# Load inventory data from CSV file
inventory_data = pd.read_csv('inventory_data.csv')

# Perform data analysis
# Example: Calculate total inventory value
total_inventory_value = inventory_data['Unit Price'] * inventory_data['Quantity']

# Generate inventory report
inventory_report = pd.DataFrame({
    'Product Name': inventory_data['Product Name'],
    'Quantity': inventory_data['Quantity'],
    'Unit Price': inventory_data['Unit Price'],
    'Total Value': total_inventory_value
})

# Export report to Excel file
inventory_report.to_excel('inventory_report.xlsx', index=False)
pip install pandas
# Inventory-Data-Analysis-and-Reporting-
