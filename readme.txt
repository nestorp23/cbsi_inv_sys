TODO:

************ WEEK 4 ************

Garrett: Display tables (DataTables) as 'cards' for mobile compatibility.

Diana: 
	- Try to fix github


Phillip:
	- Make the site mobile friendly by adding responsive CSS (so that it looks the same on desktop as it does now, but all fits properly on mobile devices and is easier to use).

Mariam:
	- Find where the Search (and input for search), Show Entries (and the input for show entries), and the 'showing' txt is added to tables by default. Then figure out how to make that extra stuff optional.

Tristan:
	- fix the error in the check-out function (sites_options($connect)) where if you dont enter a 'site' option, it still lets you check out that piece of equipment, and returns 0 as the site_id.

OTHER STUFF TO DO:
	--- Add a back button to the 'stats' page that takes the user back to whatever page they were just on before clicking the 'stats' btn

========================================================================
Hosting AWS VS GoDaddy

 AWS Option: All running in Amazon Virtual Private Cloud 
 Apache Web Server with PHP + MySQL DB running on an EC2 instance of Amazon Linux... MySQL database as Amazon RDS MySQL DB

 Pros: Very well documented with clear tutorials
 Built in security groups and easy configuration

 Cons:

 Price: Will calculate ranges using AWS CloudWatch

 Initial implementation steps
 	Create RDS DB instance (Will look into and show to our DB pros)

 	Create Amazonn Linux EC2 instance and install Apache

GoDaddy Option: Linux Hosting and MySQL over cPanel

 Pros: Seems to be a common feature of the site although documentation presented on site is very vague
 They're already using goDaddy

 Cons: Vague documentation, not as customizable as AWS, No free testing period, difficult to gauge the upfront cost
 Prices are set upfront and not based on usage

 Price: Likely Deluxe tier at 4.99/month. Need to see their current planm

 Initial implementation steps

 Obtain current plan from CBSI
 Research the process for how it is hosted and connected with the DB
 Upload files with FTP
 connect DB
 	

--------------------------------------------------------------------------


ALRIGHT - here's how to do the git stuff:


"I want to update my local files with what's on github"

	> cd C:/xampp/htdocs/cbsi_inv_sys
	> git pull

"I want to update a single file"

	> cd C:/xampp/htdocs/cbsi_inv_sys
	> git add filename.php
	> git commit -m "changelog message here"
	> git push

	*If it returns a conflict error, pull and fix conflicts, then restart this process

"I want to update all the files" (AKA push my changes to the master copy on github.)

	> cd C:/xampp/htdocs/cbsi_inv_sys
	> git add -A
	> git commit -m "changelog message here"
	> git push

"I want to add a brand new file"

	> cd C:/xampp/htdocs/cbsi_inv_sys
	> git add newfilename.php
	> git commit -m "changelog message here"
	> git push


"I want to remove my local changes and pull the version on github"

	> cd C:/xampp/htdocs/cbsi_inv_sys
	> git fetch --all
	> git reset --hard origin/master


------------------------------------------------------------------------------------------------------------------------