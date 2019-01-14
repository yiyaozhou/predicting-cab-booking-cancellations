# Predict whether a cab booking will get cancelled

## Business Context
The business problem tackled here is trying to improve customer service for YourCabs.com, a cab company in Bangalore. The problem of interest is booking cancellations by the company due to unavailability of a car. The challenge is that cancellations can occur very close to the trip start time, thereby causing passengers inconvenience.

## Competition Goal
The goal of the competition is to create a predictive model for classifying new bookings as to whether they will eventually get cancelled due to car unavailability. This is a classification task that includes misclassification costs. The winning entry will be the one with the lowest average-cost-per-booking.
Participants need to upload their classifications (0=no cancellation or 1=cancellation), and the system will compute the average-cost-per-booking based on these classifications.

## Data File descriptions
Kaggle_YourCabs_training.csv - the training set (over 43,000 bookings). Includes the output Car_Cancellation and the misclassification costs in Cost_of_error.
Kaggle_YourCabs_score.csv - the data set to be classified. Includes 10,000 bookings and no output column.
Kaggle_YourCabs_sample.csv - a sample submission file in the correct format. Your entry should include the id column from this file and a Car_Cancelled column with 0,1 values.

## Data fields
id - booking ID
user_id - the ID of the customer (based on mobile number)
vehicle_model_id - vehicle model type.
package_id - type of package (1=4hrs & 40kms, 2=8hrs & 80kms, 3=6hrs & 60kms, 4= 10hrs & 100kms, 5=5hrs & 50kms, 6=3hrs & 30kms, 7=12hrs & 120kms)
travel_type_id - type of travel (1=long distance, 2= point to point, 3= hourly rental).
from_area_id - unique identifier of area. Applicable only for point-to-point travel and packages
to_area_id - unique identifier of area. Applicable only for point-to-point travel
from_city_id - unique identifier of city
to_city_id - unique identifier of city (only for intercity)
from_date - time stamp of requested trip start
to_date - time stamp of trip end
online_booking - if booking was done on desktop website
mobile_site_booking - if booking was done on mobile website
booking_created - time stamp of booking
from_lat - latitude of from area
from_long -  longitude of from area
to_lat - latitude of to area
to_long - longitude of to area
Car_Cancellation (available only in training data) - whether the booking was cancelled (1) or not (0) due to unavailability of a car.
Cost_of_error (available only in training data) - the cost incurred if the booking is misclassified. For an un-cancelled booking, the cost of misclassificaiton is 1. For a cancelled booking, the cost is a function of the cancellation time relative to the trip start time (see Evaluation Page).
