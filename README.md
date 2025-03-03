# NFL Route Prediction

**Author:** Sajan Mehta
**Date:** January 2025
**Repository:** https://github.com/SajanMehta/NFL-Route-Prediction

---

## Project Overview
The goal of this project is to leverage pre-snap data to predict which routes NFL receivers will run. By applying machine learning classification models, the project aims to assist defensive coordinators make data-driven decisions.

## Dataset Overview:
- **Source:** NFL Big Data Bowl 2024
- **Key Columns:**
	- routeRan: The route the receiver ran
	- yardsToGo: Distance required for first down
	- scoreDifferential: The score difference (self - opponent)
	- distanceToCenter_x and distanceToCenter_y*: Shows the vertical and horizontal distance the receiver lines up from the snapper
	- timeInGame, timeInHalf: seconds left in the game/half
	- position: Position of the player (QB, WR, RB, TE, FB)

## Data Preparation:
- **Handling Missing Values:** 
	- Missing values occurred in the tracking data, in which some centers did not have positions on the field - this accounted for less than 5% of rows, and they were removed to allow the use of the distance to center variables
- **Feature engineering:**
	- **Distance from Center:** position of the center of each play was added to each receiver, and the columns were subtracted to create the variables
	- **Score Differential:** Calculated as the difference between home and away team scores

## Models implemented:
- **Logistic Regression** - Statistical Modeling for Interpretability
- **Random Forest Classifier** - Improved performance with hyperparameter tuning

## Key Steps Taken:
- **Feature Importance:** A chart was provided to visualize most impactful features
- **Hyperparameter tuning:** Improved Random Forest Classifier accuracy from **30 to 32.5 percent**

## Results and Insights:
- **Best Performing Model:** Random Forest Classifier
- **Key Takeaways:**
	- Wide Receivers run Go and Hitch routes the most by a wide margin
	- Route tendencies vary by position and the flow of the game
- **Next Steps:**
	- Implement a Neural Network for more complex pattern detection
	- Continued Feature Engineering with current modeling techniques

## Contact:
- **Email:** spmehta333@gmail.com

## Acknowledgements:
This project was created as part of the NFL Big Data Bowl 2024 competition. Thanks to the NFL for providing the dataset for this project.
