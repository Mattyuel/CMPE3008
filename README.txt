To test, run from this folder using:
python -m pytest -v

The tests simulate various functions on the website

Test login:
1/ enters valid username "standard_user"
2/ enters valid password "secret_sauce"
3/ clicks "Login"
4/ checks that it arrives at "inventory.html"
5/ validates that there is a "title" with text "Products"

Test login (invalid username):
1/ enters invalid username "bad_user"
2/ enters valid password "secret_sauce"
3/ clicks "Login
4/ checks that there is an error element with text "Epic sadface"

Test login (invalid password):
1/ enters valid username "standard_user"
2/ enters valid password "bad_password"
3/ clicks "Login"
4/ checks that there is an error element with text "Epic sadface"

Test Add to Cart (Button):
1/ Completes valid login procedure as above
2/ Selects Add to cart button for the bag product using its ID
3/ Checks the button has changed to a new ID
4/ Checks that the new ID has the text "Remove"

Test Add to Cart (In Cart):
1/ Completes valid login procedure as above
2/ Selects Add to cart button for the bag product using its ID
3/ Clicks on cart button using the button ID
4/ Checks that "inventory-item-name" element exists
5/ Checks that this ID has the correct product text (The bag)

Test Runtime:
1/ Performs the login and logout procedures
2/ Starts a timer after clicking the login or logout button
3/ Ends the timer after the clicking
4/ Test passes if the new page is recognised with 1 second