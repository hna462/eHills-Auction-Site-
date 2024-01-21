**eHills Documentation**

Creator:​ Hemanth Anantha
						
Basic Description
						
eHills Auction is a better version of eBay! eHills allows clients to log in to the server and place bids on items that are in the auction.
						
From a Programmer’s Point of View
						
Brief Overview:					
This project showcases a server-client architecture. The project uses Java Server and Client sockets, multithreading, JavaFX graphics, SQLite database, Observer pattern (observer, observable), cascading style sheets (CSS), and a synchronization of threads.
						
Features:

 JavaFX - ​Java FX enhances user experience with GUI graphics in the Client program. Each customer has a GUI-based user interface.					
Multithreading - ​Multithreading is used in both the Server program and the Client program. In the Server program, multithreading is used to handle multiple users. For every Client connected to the socket, a new thread is created; each Client runs on its own thread. In the Client program, multithreading is used to manage communication from the Server to the Client, to continuously update the Notifications window in the auction, to enable/disable Buttons and TextFields, and to continuously update the user’s Watchlist window in the auction.
						
Synchronization - ​Synchronization is used in both the Server program and the Client program. In the Server program, synchronization of two auction item timers prevents the occurrence of concurrent modification exceptions. In the Client program, synchronization ensures that all information about the auction items are updated and accurate for users.						
Sockets - ​All communication between the Server and Client objects are through Sockets.				
Observer ​- The Server program implements the Observer interface to be informed of changes in observable objects. For every Client connected to the Server, a ClientHandler is created and added as an observer to the Server. Whenever a request from the Client is processed by the Server, the notifyObservers() method is called to notify all observers of the Server of the change by a call to their update method.

 SQLite Database - ​A SQLite database is used to store all information about the seven items in the eHills auction. For each item, the name, description, minimum bidding price, “Buy It Now” price, and duration information is stored in the database.				
Cascading Style Sheets (CSS) ​- Cascading style sheets are used in the Client program to create a custom look for the JavaFX application. Three cascading style sheets are included in the Client program that contain style definitions that control the look of user interface elements.
						
List of Option Extra Features:
						
A minimum starting price greater than zero for every auction item.
 							
The duration for the auction for each item is set separately.
 							
A high limit that is a “Buy It Now” price is set for each auction item. When a customer bids that amount, he or she gets it right away.
 							
Every customer can see the bid history of every item, including who made the bid. If the item has been sold, every customer is able to see the buyer and the selling price.
 							
Items have descriptions that are visible to customers.
 							
Sound effects and a nice GUI are included in the Client program.
 							
Count-down clocks are included for all auction items.
 							
The Observable class and Observer interface are utilized in the Server program.
 							
Java SQLite database is used to store information about all auction items.
 												 						
From a User’s Point of View
						
Brief Overview:
						
Welcome to the eHills Auction! Enjoy calming cloud scenery while bidding on items you want to have.
						
Login Page Usage:
						
The start-up window you will see is the “Logon to eHills” Page. To log into eHills, you can either enter both a username and a password and then click the “Login” button, or you can leave both the username and password fields empty and then click the “Continue as guest” button. You can click the “Quit” button to exit the application.
						
eHills Auction Page Usage:
						
Once you have successfully logged into the eHills auction from the “Logon to eHills” Page, you will be taken to the “eHills Auction” page. You can press the “LOGOUT” button anytime to be taken back to the “Logon to eHills” page. On the “eHills Auction” page, there is a drop-down menu where you can select any item in the auction. Once you have selected an item from the drop-down menu, you click the “Add to your watchlist” button to add the selected item to your watchlist. When you add an item to your watchlist, the item name and all information about that item in the auction will be displayed in your watchlist. You can click the “Remove from your watchlist” button to remove the item you selected from the drop-down menu from your watchlist. When you select an item from the drop-down menu, you can enter a bid in the form “$00.00 in the field labeled “Enter your bid.” Once you have entered your bid, you will be able to press the “BID” button. Only valid bids will be accepted. A valid bid is a bid that is greater than the minimum bid price and previous high bid for that item, and on an item whose auction is not closed. An error message will be displayed if you enter an invalid bid. At the bottom of the “eHills Auction” page, notifications will be displayed to you. In the “Bid History” tab, you will be able to see when any user (including yourself) bids on an item. In the “Purchase History” tab, you will be able to see when any user (including yourself) successfully purchases an item.
						
References
						
sqlitetutorial.net - ​used in the connect() method in the DatabaseConnection class in the Server program
				 				 		
