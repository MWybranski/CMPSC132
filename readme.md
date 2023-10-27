**Inventory Management System for a Store**

This program can be used as an Inventory Management System for a store.
The program can keep track of products, manage stock levels, record
sales, and generate reports.

**List of implemented functionalities\*:**

-   **The Product class** allows you to create a product (object) with
    > the specifications of a name (string), a category (string), a
    > price (float), a quantity (integer), and an identifier (string).
    > An example of this would be product1 = Product("Product1",
    > "Category", 10.0, 10, "P001"). In this example, I created a
    > Product object and listed all the specifications required to make
    > said product.

-   **The Transaction class** allows you to create a transaction that
    > occurred in the store. In order to make a Transaction object, you
    > must have a Product object (which becomes productsold) and the
    > amount of that product that was sold (which becomes pquantity).
    > The Transaction class has a third attribute, totamount, which
    > calculates the total amount of money gained from the transaction
    > by multiplying the product sell price (productsold.price) by the
    > amount sold (pquantity). transaction1 = Transaction(product1, 5).
    > In this example, a Transaction object is created with the product
    > sold being product1 and the amount that was sold being 5 items.

-   **The Inventory class** supports various methods that can be used to
    > add a product to the inventory, manage the product's stock,
    > retrieve information about the product, etc. When an inventory
    > object is created, it also creates two empty lists,
    > currentInventory and transactions. inventory1 = Inventory()
    > creates the inventory object, inventory1.

    -   **add_products** appends a product object in the list
        > currentInventory. inventory1.add_products(product1). In this
        > example, inventory1's add_products method is called with
        > product1 being its argument. product1 is appended into
        > currentInventory.

    -   **increase_stock** takes a Product object and a certain amount
        > of objects (integer) and adds the amount to the Product
        > object's quantity attribute. The method sets the object's
        > quantity attribute to the sum previously mentioned.
        > inventory1.increase_stock(product1, 3) will increase
        > product1's quantity by 3. It will go from 10 to 13 (or 7 to 10
        > if this method is used after decrease_stock).

    -   **decrease_stock** takes a Product object and a certain amount
        > of objects (integer) and subtracts the amount from the Product
        > object's quantity attribute. The method sets the object's
        > quantity attribute to the difference previously mentioned.
        > inventory1.decrease_stock(product1, 3) will decrease
        > product1's quantity by 3. It will go from 13 to 10 (or 10 to 7
        > if this method is used before increase_stock).

    -   **retrieve_info** asks the user an input on what information
        > they would like to see from the Product object the user puts
        > in as the argument when they call the method.
        > Inventory.retrieve_info(product1). You need to call the class
        > here (not the Inventory object) because you do not need any of
        > Inventory's attributes when using this method. When the
        > command line pops up on screen you can look for a specific
        > piece of information about the object. If you type in:

        -   Name = "Product1" (the Product object's name)

        -   Category = "Category" (the Product object's category)

        -   Price = 10.0 (the Product object's price)

        -   Quantity = 10 (the Product object's quantity)

        -   Identifier = "P001" (the Product object's identifier)

        -   Something other than the above words = \"You must enter a
            > specific piece of information you would like to see\"

    -   **record_transaction** uses a Transaction object to check if a
        > productsold object (Product object) is in currentInventory and
        > if that object's quantity is less than the quantity sold in a
        > transaction. If both of these are false, then the method
        > appends a tuple (made up of productsold and pquantity) to the
        > transactions list created when an Inventory object is created.
        > It also decreases the product sold's quantity with the
        > quantity that was sold during the transaction.
        > inventory1.record_transaction(transaction1) In this example,
        > transaction1 is used as the argument and it is recorded into
        > the transaction list because it is not in currentInventory and
        > it sold less of product1's stock.

    -   **stock_levels_report** takes the currentInventory list of an
        > Inventory object and, for each Product object in the list,
        > prints out a message that lists the object's name and
        > quantity. inventory1.stock_levels_report() In this example,
        > the result would be "The current report on stock levels:
        > Product: Product, Quantity: 5" because this is the only
        > product in the list.

    -   **sales_history_report** takes the transactions list of an
        > Inventory object and, for each Transaction object in the list,
        > prints out a message that lists the Product object's
        > (productsold) name, the quantity sold, and the revenue of the
        > transaction (by multiplying the Product's price and quantity
        > sold). inventory1.sales_history_report() In this example, the
        > result would be "The current history report on sales: Product:
        > Product, Quantity Sold: 5, Total Amount: \$50.0" because
        > transaction1 is the only item in the transaction list for
        > inventory1.

    -   **revenue_report** creates a variable, total_revenue, that
        > starts at 0. For each Transaction object in the list of
        > transactions, the product of productsold's price and pquantity
        > is added to the total_revenue. When there are no more
        > transactions in the list, the total revenue is printed out.
        > inventory1.revenue_report() In this example, the result would
        > be "The total revenue is \$50.0" because transaction1 is the
        > only transaction in the list, its product is the only
        > iteration of total_revenue.

**\* Read the class/method description before using said class/method.
Examples for each class/method are provided in the code.**
