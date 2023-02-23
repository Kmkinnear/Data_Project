# Titanic Data Project

## Purpose

The purpose of our project was to use Machine Learning to build a predictive model that accurately predicts whether a passenger survived or died during the sinking of the Titanic. The original dataset had eleven features and one target variable that we would use to manipulate our data. We will create dataframes using Pandas in Jupyter Notebook that we will assist us in cleaning up and analyzing our data. We will experiment with different models and ultimately decide on one model that we are happy with.

## Analysis

### Decision Tree Classifier

We ended up going with using a Decision Tree model for our analysis in this project. We really like how we could see how the model worked its way through features and predicting the outcomes. We can see in the model that the colors range from shades of blue to shades of orange. For the purposes of this model, the blue portions represent those more likely to survive and the orange represents those that are likely non-survivors. We can see that there is a heavy concentration of predicted survivors to the left side of the tree with a mix of predicted survivors on the right side of the tree which is comprised mostly of predicted non-survivors. We can zoom in and see how the model split at each layer and see which features the model viewed as being more important.

![image](https://user-images.githubusercontent.com/110848660/220732551-5779afc8-ebf3-4a9e-8030-1b39229052ca.png)

This model is a little overwhelming to begin with so to make it easier to work with, we included a parameter to set the maximum number of layers to three. This allowed for an easier model to visualize and present. It's also easy to see how each level was split and was feature it was split off of. In the model below, we can see that the features were ranked in importance from Male (Gender), Pclass, Family, and Age. We see that by using a 3-layered model, a significant determinant of survival was whether the passenger was male or female.  

![image](https://user-images.githubusercontent.com/110848660/220732631-8859cbff-ce61-406e-9fe3-0a3273df3330.png)

![image](https://user-images.githubusercontent.com/110848660/220737729-ada2568c-1325-442f-ae44-28f03efc7469.png)

## Results

### Confusion Matrix

![image](https://user-images.githubusercontent.com/110848660/220732762-a9126904-46a3-4640-ac95-002d5476d8aa.png)

- True Negatives (Predicted Died, Died) – 167 Passengers
- False Positives (Predicted Survived, Died) – 47 Passengers
- False Negatives (Predicted died, Survived) – 48 Passengers
- True Positives (Predicted Survived, Survived) – 70 Passengers

### Classification Report

![image](https://user-images.githubusercontent.com/110848660/220732798-57852669-7c4b-40c4-9f36-5fe83532803a.png)

We can see that our model did well overall. We were able to attain an accuracy score of 76%. This was in line with all the other models that we experimented with, which was good to see. We can see that our precision scores were very similar with 76% and 74%. However, our model did not do as well with the recall scores. We can see that our model only scored at 61% with being able to accurately predict actual survivals. This compared to a score of 86% at being able to accurately predict actual deaths.

Tableau Visualization Dashboard: https://public.tableau.com/app/profile/guy6801/viz/TitanicProject_16762110932600/TitanicProjectDashboard

## Summary

We believe our model did a sufficient job at predicting survivors and non-survivors with the dataset and features that we gave it. As we mentioned above, our model was able to achieve an accuracy score of 76%. 

There are numerous ways that we can further test the data to see if we can achieve better results with the model. One thing would be to change the size of our training and testing group size. The only concern there is to make sure we have enough training data and that we also don't overfit our model. We could also explore additional predictive learning models to see if there is one out there that performs any better than the ones we previously tested. We also ran our model with 4 features (Gender, Pclass, Family, and Age) out of the 11 that were initially provided in the data. We could experiment with adding more features or remove some of the ones we worked with to see how it affects the performance of the model.

Technologies Used:
- Jupyter Notebook (Pandas, Sklearn, Various Visualization Packages)
- Python
- Tableau
- PowerPoint

Data Source: https://www.kaggle.com/competitions/titanic
