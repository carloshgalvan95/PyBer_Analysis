# PyBer_Analysis
---

## Overview of the Analysis
PyBer is a mobility as a service provider, allowing users to book a car and a driver to transport them in a way similar to a taxi.

After running an analysis based on data obtained from rides among different type of cities (Urban, Suburban and Rural). The main takeaway found was a visible disparity between the fares for each ride. To address this issue and to derive insights and obtained suggested measures to take.

## Results
We have two datasets to work with. The first dataset gives us the driver count and type of city of several cities where PyBer provides services. The second dataset provides more detailed information of specific rides, through this dataset we can easily analyze the fluctuations of fares for every city type.

To be able to use this information, we are going to first merge both dataset to use them in conjunction.

![Pyber_Dataset](https://github.com/carloshgalvan95/PyBer_Analysis/blob/main/Analysis/Pyber_Dataset.png)

To visualize the disparity noticed, we are going to use three main comparisons.
- **Total Rides by City Type**
- **Total Drivers by city Type**
- **Total Fares by City Type**

### Total Rides by City Type
What we notice here is the expected, urbanized cities get a considerably higher amount of rides than suburban or rural cities.

This is of course translated to more job opportunities for each driver that register to provide services with PyBer and generally speaking the more rides generated, the more revenues obtained.

Nevertheless as any other product or service in the market, the value is determined by the law of supply and demand.

>*The law of supply states that the quantity of a good supplied (i.e., the amount owners or producers offer for sale) rises as the market price rises, and falls as the price falls. Conversely, the law of demand says that the quantity of a good demanded falls as the price rises, and vice versa.*
*-* ***Al Ehrbar. Supply and Demand [Econlib](https://www.econlib.org/library/Enc/Supply.html#:~:text=The%20law%20of%20supply%20states,price%20rises%2C%20and%20vice%20versa.)***

Taking into account this principle, we can assume that the fares are going to decrease the more drivers we have.

![Pyber_TotalRides](https://github.com/carloshgalvan95/PyBer_Analysis/blob/main/Analysis/Pyber_TotalRides_CityType.png)

### Total Drivers by City Type
As we previously discussed an determined, the amount of drivers is going to impact the average fare for each ride. Even if we get more rides, if the fare decreases, we can get to a point of diminishing returns where, as counter intuitive as it may sound, it could be in our best interest to lower the amount of hired drivers to decrease the total of rides and subsequently, the average fare.

![Pyber_TotalDrivers](https://github.com/carloshgalvan95/PyBer_Analysis/blob/main/Analysis/Pyber_TotalDrivers_CityType.png)

### Total and Average Fares by City Type
Finally, we are going to analyze the fare tendency for every city type to confirm our hypothesis. We can analyze this information with multiple approaches:
- #### Total Amount of Fares for each City Type

| **City Type** | **Total fares ($ USD)** |
|-----------|---------------------|
| Urban     | $ 39,854.38         |
| Suburban  | $ 19,356.33         |
| Rural     | $   4327.93         |

The results from this table are just as expected, given that Urban cities are going to be way bigger and the size as well, the revenues are going to exponentially increase from suburban and rural cities. The main takeaway is going to be asking the questions, *How can we balance the number of drivers in Urban cities to mantain the same revenue while also increasing the average fare?*

- #### Average Fare per Ride

| **City Type** | **Average Fare per Ride ($ USD)** |
|-----------|-------------------------------|
| Urban     | $ 24.52                       |
| Suburban  | $ 30.97                       |
| Rural     | $ 34.62                       |

Now, let's evaluate the tendency of fares for each city type. As per the law of supply and demand, we clearly see here that the amount of drivers available in Urban cities is decreasing the average fare per ride, this is not benefitial in two main aspects. First, using PyBer in Rural cities is going to be less attractive, lower distances but more expensive fares in addition to the fact that people living in rural cities are more used to not use a car that often is going to make really difficult to portray PyBer as an attractive alternative for transportation. Second, Ironically, the bigger is not always the better, every driver added to PyBer signifies an additional point of possible failure, the more variables you have, the more possible point of failure, sometimes is better to have quality than quantity, if we can mantain our revenues intact by increasing the average fare and decreasing the amount of drivers, the points of failure decrease.

- #### Average Fare per Driver

| **City Type** | **Average Fare per Driver ($ USD)** |
|-----------|---------------------------------|
| Urban     | $ 16.57                         |
| Suburban  | $ 39.50                         |
| Rural     | $ 55.48                         |

We can see an even bigger disparity between the average fares here confirming the hypothesis. Having this information we can determine how our average fare is going to vary by each driver and determine a point of diminishing return for the amount of total drivers.

## Summary
---
![PyberSummary_LineChart](https://github.com/carloshgalvan95/PyBer_Analysis/blob/main/Analysis/PyBer_fare_summary.png)

After evaluating our three points of analysis we can clearly see a disparity between the average fare for rural and urban cities. This represents a problem given that It can be discouraging as a driver but also for the company to have such a huge difference on revenues. Even though, considering the total revenues and amount of rides this disparity get compensated and the revenues in urban cities are way higher that in rural ones. The possible approaches to address this problems is as following:

1. As previously mentioned if we can balance the average fare for urban cities while also decreasing the amount of drivers and mantain the same amount of revenues identifying out point of diminishing returns, the quality of service could be increased and the points of possible failure decreased. If we are obtaining *y* amount of revenue a year with *x* amount of drivers, with certain amount of rides *c*, given a determined fare *f*, *(cX)x f = Y*. If we can *f* and *c* are correlated we can determine a point where decreasing the drivers is going to still result in the same amount of revenues *Y*.

![Ride_Fare_Data](https://github.com/carloshgalvan95/PyBer_Analysis/blob/main/Analysis/Fig4.png)

2. A different approach to this, less problematic but also prone to other errors, would be to simply determine a set fare for each ride given the type of city and distance not influence by the law of supply and demand elimination the variable factor but that could also bring problems with the customer acceptance of this fare increase.

3. It would also be benefitial for further analysis to be done to determine wheter is better or worse to invest in providing services in rural cities with a set minimum population and size or just investing those funds in increasing the coverage in additional urbanized cities.

![Ride_Sharing_Data](https://github.com/carloshgalvan95/PyBer_Analysis/blob/main/Analysis/Fig1.png)

