# pac_members


To do 

* Batch upload current emails and data after deployment
* DONE-- Figure out how to handle people who have already paid, and prevent them from paying early (probably just not allow anyone who's prior to expiration to pay, this is simplest, with different messages. maybe the way you email is 2 weeks ahead for subscribers, and when it expires for anyone who wasn't subscribed)
* DONE-- Re-do routes to only use what you need
* DONE-- Abstract out the functionality for the stripe charging into a service
* DONE-- Add first and last name to sign up
* NEED TO CONFIRM-- Auto email two weeks ahead of expiration - use "whenever" gem. 3 cases: on membership and will renew (link to cancel), off membership and will expire, off membership and has expired
  * DONE-- Create Mailer
  * DONE-- Create functions to send separate emails
  * DONE-- Add method function to scan all users
  * DONE-- Add whenever job
* DONE-- Rather than create, force it on the backend so we can ask why people are cancelling, create an admin tool to do it. Create cancel subscription page (remove 'auto_renew' from field)

* DONE-- Style everything
* DONE-- Add Active Admin
* Enable receipt emails from Stripe (when live)
* Add cron job to let people opt in to auto-charge their CC and add to subscription if not on renewing plan? -> this is for the two weeks out prior to expiration thing, this also requires you to edit the mailer
* DONE -- Set up environment variables on heroku
* Test payment on live server

* Set up domain

* DONE-- Add new fields to user
	* membership_expiration date
	* stripe customer_id
	* subscription_id
	* auto_renew (on/off)
	* mailchimp or square data?
	* First and Last name
	* Any other fields from the original form on SquareSpace?

* HTTPS? - probably don't need with Stripe checkout.js

* All the other integrations (document)
  * Mailchimp
  * Square
  * Picatic
  * Apparently its just going to be importing all the data...

* Sign in webpage on tablet for events? (Works w/ Picatic + our membership db?) Or is Picatic just good enough
* Auto generate promo codes for users during events

* Phone numbers and mailing addresses -> add fields to sign up screens
* Create csv importer for old people <- add the actual stripe plans first to save yourself some god damn hassle!
* DONE - Create "youve been signed up here's your password" email
* DONE -Boot them to the "contact info" page for them to fill out. You should probably draw a flow diagram for the different situations
* Walk through sign up flow to make sure its reasonable