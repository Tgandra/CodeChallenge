
Objective

1) FlightSearch.json . This JSON Schema includeds objects related to Book a Flight from AlaskaAir
https://www.alaskaair.com/planbook?lid=nav:book-flights&int=AS_NAV_Book_Flights_-prodID:ShoppingBooking

2) FlightSearchReesult.JSON captures the objects/data related to flight results

3) Booking.Json captures the transaction related event information 

4)We can answers below Questions from objective
   -What is the conversion rate for an individual flight search result? 
        Assumption : single user do multiple searches,So when we say conversion rate what is this based on ? how many searches resulted as bookings?
        or how many users booked?
    With booking data we can calculate total number of users completed the transaction vs total number of searches as Conversion rate

   -How does the cost in miles affect the guests’ willingness to purchase? For this question, assume that the conversion space is already tagged successfully, and this data is already accessible.
     "Use miles" option on search will provide results with miles and with booking type value from trasactoion we can identify if a user chosen to pay with Miles for booking.
	
   -How many times does a guest attempt to search for a destination that we do not serve for the given airport or date?  
    every search returns a search id with response "success" or "failure" . we can calculate total number of failures in a given period using serach results.
5) DataStrategy and Storage 
   - We can store this data in Blobs/Lakes in parquet orr any format and transfrom same to SQL with databaseobjects designed at highlevel
   - also we can use azure delata lake capabilities to cpature only delta events and databricks.
   
   
   
PS:
  i have provoided MS Azure solutions in tools.
 
