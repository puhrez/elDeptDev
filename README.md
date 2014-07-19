#El Deptartamento de la Comida
###Set-Up
**TODO:**
- Move DNS hosting to simpledns.com
- Move hosting to and open an account on AWS
- Run a node.js EC2 server
- FOR DEV: Run a MongoLab server for DB

###App
####Features:
**TODO:**
- Identity:
    - About Us
	- Who Are We?
	- Where are we?
	- Contact
    	- Mission
    	- Vision
    	- Philosphy
  - Events
    - Google calender
      - Sync with facebook?
  - Programs
    - Transportation
    - The Store
    - Agriculture Consulting
  - Resources
    - Articles
    - Cultural Seed Bank
  - Become a Member!
- Farms:
  - Farm map
- Online Store:
  - On sale
  - Coming this week
  - What's in
####Design:
**TODO:**
- Splash About Us:
  - Rotate Circle, Shift left, fade-in right Name, shift up, fade-in down content
- Color Scheme

**FILL THIS IN ALBERTO**
###Internals:
**TODO:**
- POS:
   - Secure route
   - employee id + password for auth
   - form
	- Produce Name (drop-down pick)
	- Farm of Origin
	    - This will connect it to the Order ID
	- Quantity
   * upon send:
	- insert to sales collection with timestamp, user info, in-store: true
        - update to inventory to reduce the number of produce by quantity
   * return with:
	-  total price
- Order log
   - Secure route
   - employee id + password for auth
   - form:
	- Farm of Origin
	    - Name of Farmer
	    - location of Farm
	- Produce
	    - Name of Produce
	    - Quantity
            - Quality
	    - Price
    * upon send:
	- insert to orders collection with timestamp, user-info
	- upsert to inventory to add the new produce
###DataBase:
####DBs:
**TODO:**
- AgroBase
  - Cultural Seed Bank
- Inventory
  - Produce
	- Cross reference with Farm Ids
  - Payment
	- uses order id's timestamp to notify admin on what order payments need to be verified
- Farms
  - Farm contact
  - Farm ID for inventory reference

