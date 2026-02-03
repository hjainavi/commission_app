# Commission App

A desktop application built with Python Tkinter for viewing daily sales commission of employees. The application connects to an Oracle database to fetch and display sales data with commission calculations.

## Features

- View daily sales commission for each salesman
- Date picker for selecting specific dates
- Navigate between salesmen using Previous/Next buttons
- Hierarchical view of bills with line item details
- Automatic commission calculation based on discount percentages
- Sortable columns in the data grid

## Technologies Used

- **Python 2.7** - Core programming language
- **Tkinter/ttk** - GUI framework
- **cx_Oracle** - Oracle database connectivity
- **Oracle Database** - Backend data storage

## Prerequisites

- Python 2.7
- Oracle Client installed
- cx_Oracle library
- Access to Oracle database with RICHIERETAIL schema

## Installation

1. Install Python dependencies:
```bash
pip install cx_Oracle
```

2. Ensure Oracle Client is installed and configured on your system

3. Update database connection settings in `commission.py`:
```python
ip = '127.0.0.1'
port = 1521
SID = 'your_sid'
```

## Usage

Run the application:
```bash
python commission.py
```

### Commission Calculation Logic

- If discount >= 10%: Commission = 1% of net amount
- If discount = 0%: Commission = 2% of net amount
- Otherwise: Commission = 2% of item price - 10% of discount amount

## Files

| File | Description |
|------|-------------|
| `commission.py` | Main application with GUI and business logic |
| `calendar_custom.py` | Custom calendar widget for date selection |
| `ttkcalendar.py` | Calendar dialog implementation |
| `tkSimpleDialog.py` | Simple dialog utilities |

## Screenshot

The application displays:
- Bill number with subtotal, discount, net amount, and commission
- Expandable rows showing individual line items
- Total commission for the selected date and salesman

## License

This project is proprietary software developed for internal business use.
