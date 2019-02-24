## CoffeeForMe
Sell beverages and view/export sales records with CoffeeForMe command-line application.
Supports Python 3.6+.

There are 2 roles in the app: **Salesperson** and **Manager**.

Salesperson can sell _beverages_ (e.g. Tea, Coffee, Water, Soda, etc.) and _ingredients_ (e.g. Sugar, Milk, Cinnamon, etc.). Once the sale is done, salesperson's sales details will be printed and stored at project root inside **salesperson_records** folder with file name **FirstName LastName_records.txt**.

Manager can view salespeople's sales records (printed as a table) and export records as json, xml and csv files. Sales records are stored at project root inside **manager_records** folder with file names **FirstName LastName_records.json**, **FirstName LastName_records.xml**, **FirstName LastName_records.csv**.

Once the app is started, HELP will be printed:
```
usage: coffee_for_me [-h] [-bev BEVERAGE] [-add ADDITION]
                     employee_name employee_position

Sell drinks and view sales records with "CoffeeForMe!"

positional arguments:
  employee_name         Employee name
  employee_position     Employee position (Salesperson or Manager)

optional arguments:
  -h, --help            show this help message and exit
  -bev BEVERAGE, --beverage BEVERAGE
                        List of available beverages a Salesperson can sell:
                        tea, coffee, water, soda, etc.
  -add ADDITION, --addition ADDITION
                        List of available ingredients a Salesperson can add:
                        sugar, milk, cinnamon, etc.

Thank you for using "CoffeeForMe" App!
```

1. Clone the repository.
2. Run ```python pip install -e .``` from project root folder to install the app in development mode. Each time you make any code changes, just run the command again and and you will get the app with your updates.
3. As a Salesperson run ```python coffee_for_me Tony Salesperson -bev=Tea -bev=Coffee -bev=Water -add=Sugar -add=Milk -add=Cinnamon``` to make a sale. You can provide any number of beverages and ingredients.
4. As a Manager run ```python coffee_for_me Anna Manager``` to view and export sales records.
5. Run ```python coffee_for_me -h```  to see Help.
6. To run unit tests navigate to ```cd /coffee_for_me/tests``` and run ```python -m unittest -b```. Failed tests if any will be outputted.