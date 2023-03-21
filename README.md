# MySQL
H/t 10/03/23
(1) вывести название товаров из 2 и 5 категории с ценой от 5 до 25 (EURO), где в названии есть слово 'syrup'
SELECT * FROM [Products]
where (CategoryID in (5, 2)) 
and (Price between 5 and 25) and 
ProductName like '%syrup%'

(2) добавьте произвольный товар в таблицу Products
INSERT INTO [Products](ProductName) values ("Cheese")

(3) у клиента с ID 1 измените адрес на произвольный
UPDATE [Customers]
SET Address = "Flowers Str. 1"
Where CustomerID = 1

(4) у всех клиентов не из Гермарнии и не из США очистите адрес и контактное имя
UPDATE [Customers]
SET Address = "", ContactName = ""
Where NOT Country in ("Germany", "USA")

(5) у всех поставщиков (Suppliers) очистите номер телефона
Update [Suppliers]
SET Phone = ""

(6) удалите всех поставщиков не из 'USA'
delete from [Suppliers]
where Not country = "USA"
