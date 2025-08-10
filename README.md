Normalization – HW2
1NF
Valori atomice; despachetam „Product_title and quantity”.

Tabele intermediare:

OrderLines_1NF(OrderNumber, ProductTitle, Quantity, Client, ClientAddress, OrderDate)

2NF
Introducem produse ca entitate separata (evitam dependenta partiala).

Products(id, name, description)

OrderLines_2NF(OrderNumber, ProductId, Quantity, Client, ClientAddress, OrderDate)

3NF (final)
Eliminam dependentele tranzitive (datele de client stau la client).

Customers(id, name, contact, address, city, postal_code, country)

Orders(id, customer_id, order_date)

Products(id, name, description)

Order_Items(order_id, product_id, quantity)

Chei straine: Orders.customer_id → Customers.id, Order_Items.(order_id, product_id) → Orders.id, Products.id
