# Renovation Research
Eli Ingleson and Bryan Arteaga


# Overview and Business Problem
Recently, a client came to us named Teddy. Teddy is in the business of buying, renovating, and then selling homes for a profit. Teddy has just bought a new house in a middle-class neighbhorhood. He is curious to know kind of renovations he can do to make the most profit on his new project. 

# About the Data
For this project, we utilized the data from the [King County Data Assessor Website](https://info.kingcounty.gov/assessor/esales/Glossary.aspx?type=r). The data within had information about housing sales in King County, Washington. It had 21,597 rows of data with each row having individual information about a particular house. Some examples include the square footage of the house, whether or not it has a view, how large the lot is, and the condition and overall grade of the home. 

# Methods
As mentioned above, Teddy has already bought a house in a middle-class neighborhood. Because of this, we wanted to work with data pertaining to middle-class homes. To get this data, we took the average price of the homes in the dataset and anything within one standard deviation of that average was included in a new dataset. 

After that, we looked at what variables Teddy could actually manipulate in his renovation. He could not control whether or not the house has a view or is on a waterfront. Therefore, we dropped a lot of the columns such as view, waterfront, latitude, longitude, and a few others. However, we kept zipcode because we had a large increase in the accuracy of our models after adding it back.

# Modeling
We began our modeling with creating two baseline models. The first compared the square footage of the house with price, and the second compared the number of bathrooms to price. Neither of these had terrific results, but with so much of the data excluded, we were unlikely to get terrific scores.

After our basline models, we moved onto some more experimental models and put more variables in. We used new variables like condition and grade. We also created new variables such as the ratio between bedrooms and bathrooms or how large the house is in relation to its lot size. After several models, we found a model we thought we could advise Teddy on, and this became our final model.

# Final Model
We chose our final model to include the bathroom-bedroom ratio, grade, condition, the square footage of the home, and the zipcode. This gave us a an R-Squared value of .78 which was our highest value behind our kitchen-sink model at .8. Because there were less variables in our this model, we thought it was the best one to advise our client on.
# Conclusion
According to our final model, we would recommend our client to expand the size of the house as that has been the most consisent way of raising the overall price of the house. Increasing the square footage of the house by one unit will lead to the price increasing by $106. Our client can do this by adding another floor, more bathrooms or bedrooms, or just expanding the overall size of the house. Furthermore, we also found a strong correlation between the overall grade of the house and the saleprice. Higher grade materials create higher values. However, our models cannot predict how much the renovation will actually cost or if it is even worth doing; however, we see a strong correlation between square footage and grade with price. Another thing we would advise our client on is that not all of our models are enitrely accurate because we cut so much of the original data out. If we had more time, we would like to see how we could make our models more accurate given our abbreivated dataset.

# Repo Navigation

```
├── Notebooks        <- Working notebooks.
├── License          
├── Final Notebook   <- Report Notebook
├── README.md        <- The top-level README for developers using this project.
├── utils.py         <- Imported Function
```