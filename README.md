Location of Jupyter Notebook within GitHub:
https://github.com/SanjayRRavi/Module11_PracticalApp/tree/main
(Detailed work and plots are shown here)

Business Problem Statement: 
Objective here is to provide a used car dealership, the client, recommendations on what the customer values in a used car. In order to achieve this, we need to understand the factors that make a car more expensive, since the car dealers will need to communicate to the end clients what features would be missing if the client is looking for cheaper cars, and also what features need to be present if they want to sell expensive cars to more clients. Data analysis will need to be done to understand which factors correlate well to used car prices and which don't.


Summary and Key Findings: 
Polynomial regression model of degree 3, a cubic model, has been created and selected as the most optimal, in order to predict used car prices using certain characteristics that are considered to be most important for a typical used vehicle. These findings below from the model correlate closely to the pre-model data analysis that was done.

Since the model output is normalized or scaled, in order to convert the model output value into real-world vehicle price, we need to use this formula:

vehicle_price = predicted_value x standard_deviation + mean

standard_deviation = y.std() within this notebook (standard deviation of all the vehicle prices)
mean = y.mean() within this notebook (average of all the vehicle prices)

The question of which features drive used car prices up and which features drive used car prices down are answered below using this model:

Most important features that drive used car prices up:
Year of the vehicle (newer vehicles will cost more compared to older vehicles)
Diesel fuel
Vehicle needs to be either all-wheel drive (AWD/4WD) or rear-wheel drive (RWD)
Vehicle needs to be either a truck or a pickup
8-cylinder vehicles
Other types of transmission, which are neither automatic nor manual. Specifics of "other" to be determined by the used car dealers.

Most important features that drive used car prices down:
4-cylinder vehicles
odometer mileage

Recommendations for the used car dealers:
Increase the stock of vehicles which fall in the category of features driving prices up, mentioned above. This includes the high end large vehicles, such as trucks and pickups, which typically use 8-cylinder and diesel fuel and are all-wheel drive. Also it is necessary to make sure only the newer used cars with less total miles driven are brought into stock.
Reduce the stock of vehicles which fall in the category of features driving prices down, mentioned above. This includes 4-cylinder vehicles as well as older vehicles with more total miles driven.
The features driving used car prices up are the ones that customers want to see.

Disclaimer:
This model has certain limitations, where not all of the features can be incorporated into the model due to constraints in computational time and resources.  Therefore, this model includes only the most important features. 
