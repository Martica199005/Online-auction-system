# Online-auction-system

Problem Description
An auction house has contacted you to implement an online auction system. Into the
currently the auction house has a web platform where customers can create an account to
view details of products sold, and administrators can register new products.
With the transition to the online environment, the auction house decided to hire brokers to
mediate customer auctions.
The following types of entities used by the application are defined:
● Product, with properties int id, String name, double Sale price, double Minimum price, int
year
○ Painting, with properties: String namePainter, Enum colors (oil, tempera or
acrylic)
○ Furniture, with the properties: String type, String material
○ Jewelry, with the properties: String material, boolean stoneIso price
● Employee
○ Broker, with the properties Client_list and clients
○ Administrator
● Client, with properties: int id, String name, String address, int noParticipations, int
noLicitation iiCăș tigate
○ Individual, with the properties: String dataBirth
○ Legal entity, with the properties: Enum company (SRL or SA), double
Social capital
● Auction, with properties: int id, int noParticipants i, int idProduct, int noMaxim Step
● The auction house maintains:
○ List of Products for sale
○ Customer List in the system
○ List of Active Auctions
Key features:
● The products sold by the Auction House are stored in a list that Customers can
view, Brokers can change it by deleting (selling) products, and
Administrators can change this by adding new products. These entities can
work with the list at the same time
● Customers who want to bid for a product request this from the Auction House
specifying the desired product id. The auction house randomly associates a
Broker to each Client, and the Broker mediates the auction later
● The broker applies a commission for each associated Client. There are several algorithms
commission calculation, which differs depending on the Client and his history:

○ C1 - 20% of the value traded by the Client for Individuals who
they bid less than 5 times
○ C2 - 15% of the value traded by the Client for Individuals who
they bid more than 5 times
○ C3 - 25% of the value traded by the Client for Legal Entities which
they bid less than 25 times
○ C4 - 10% of the value traded by the Client for Legal Entities which
they bid more than 25 times
Bidding mechanism:
1. A Customer sends a request to the Auction House for a particular product, identified by
id. At the same time set a maximum price that you can pay for one
Product
2. The auction house randomly associates a Broker with the Client
3. The auction house starts the auction when the number of registered participants is equal to
nrParticipants and announce all start Brokers
4. An Auction ends after the iMaxim Step no. The product is sold to the customer who offers
at most, as long as the offer is greater than or equal to the Minimum Price of the Product.
Otherwise, the product is not sold. If at the final step several Customers offered
the same amount for the Product, is sold to the one who won the most Auctions
5. At each step of the Auction Brokers ask Clients for the bid they submit
away from the Auction House. The auction house calculates the maximum amount offered for each
step, inform the Brokers about the maximum amount, and they inform further
customers
6. A Customer may use any algorithm to calculate the bid. The amount is not
may exceed the maximum price set in step 1
7. After the No iMaxim Step The auction is stopped, Customers are notified of the result and ends
communication between Brokers and Clients

Your application must meet the following constraints:
● The project will run at least 10 tests
● Number of entities per test - o Auction House, one Administrator, minimum 6 Customers,
minimum 2 Brokers, minimum 20 Products (of different types), minimum 4 Auctions
Remarks:
● The minimum number of participants in an Auction is 2
● All Brokers participate in an Auction
● A Client can participate in any Auctions
● The Client communicates directly with the Auction House only when registering for the Auction
● In addition to the entities described by the application, they may have other fields in addition to those
described in the statement
Must be implemented:
● 2p - Multithreading
● 2p - Implementation of at least 4 reasoned design patterns (0.5p / design pattern)
● 2p - Genericity
● 2p - Testing the application with at least 10 scenarios (input read from file or hardcoded in
application)
● 2p - Using OOP concepts (encapsulation, inheritance, abstraction, polymorphism)
● 0.5p bonus - clean code - simple code to understand, methods and representative classes
(according to SOLID principles - especially single responsibility), consideration
recommendations for improving the code using SonarCube / SonarLint
● 0.5p bonus - unit testing (at least 10 unit tests for the major functionalities of
application)
● 0.5p bonus - early bird (presentation before deadline)
● 0.5p for a wow implementation / functionality that will impress even
presentation assistant (e.g., cutting edge features in Java, lamda expressions,
something catchy)
depunctare
● -3p - The auction house communicates with the Client without the Broker
● -1p - Inadequate coding style
● -1p - No comments (both ReadME and comments in code / Javadoc)
