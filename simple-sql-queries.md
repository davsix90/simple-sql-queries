Find the average length of all tracks in Milliseconds
    SELECT AVG(Milliseconds)
    FROM Track
        AVG(Milliseconds) = 393599.2121039109

Find the number of invoices in the USA
    SELECT Count(BillingCountry)
    FROM Invoice
            WHERE BillingCountry = "USA";
            Count(BillingCountry) = 91

Make a list of all the First Names of Customers that contain an 'a'
    SELECT *
    FROM Customer
	    WHERE FirstName LIKE "%a%";

Make a list of the 10 longest tracks
    SELECT *
    FROM Track
        ORDER BY Milliseconds
        Limit 10

Make a list of the 20 shortest tracks
    SELECT *
    FROM Track
        ORDER BY Milliseconds DESC
        Limit 20

Find all the customers that live in California or Washington
    SELECT *
    FROM Customer
        WHERE STATE = "CA" OR STATE = "WA"

Find all the customers that live in California, Washington, Utah, Florida, or Arizona (Use IN keyword)
    SELECT *
    FROM Customer
        WHERE STATE IN ("CA", "WA", "UT", "AZ", "FL")

Insert an artist to the database
    INSERT INTO Artist(Name)
    VALUES ('Eminem') 

Insert yourself as a customer to the database
    INSERT INTO Customer(FirstName, LastName, Company, Address, City, State, Country, PostalCode, Phone, Fax, Email, SupportRepid)
    VALUES ('David', 'Sixta', 'Vivint Solar', '1234 NoWhere St', 'Whoville', 'UT', 'US', '12345', '555-5555', '', 'cantTouchThis@gmail.com', 6)    

Find a list of all Playlists that start with Classical


You can either continue exploring this dataset or look into setting up postgres on your local machine.