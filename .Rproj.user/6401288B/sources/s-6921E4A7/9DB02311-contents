## The Average in R: mean()

# R provides an extremely straightforward way of calculating the mean of a set of 
# numbers: mean(). I apply it to the example of the heights of six children.

heights <- c(36, 42, 43, 37, 40, 45)
mean(heights)

# we have a dataset called "Cars93" in the MASS package.
# After importing it, I want to find out the average horsepower of cars made in the USA
Horsepower.USA <- Cars93$Horsepower[Cars93$Origin == 'USA']
mean(Horsepower.USA)

# note how the brackets allow us to filter the dataset by categorical variables
# This function, with() allows us to avoid using "$"
with(Cars93, mean(Horsepower[Origin == 'USA']))

# we can append another condition of the filtering with "&" like so:
with(Cars93, mean(Horsepower[Origin == 'USA' & Cylinders == 4]))

# trim() function: calculates a statistic, removing outliers
mean(Horsepower.USA, trim = 0.5)

## EXPLORING THE DATA
# Lets visualize the overall distributions for the horsepower variable and facet by the 
# origin variable
ggplot(Cars93, aes(Horsepower)) + geom_histogram(color="black", fill="white",binwidth = 10) + facet_wrap(~Origin)

# how many cars are in group of cars that originated in the U.S.?
with(Cars93, length(Horsepower[Origin == "USA"]))

# What is the standard deviation of this group
with(Cars93, sd(Horsepower[Origin == "USA"]))

# calculate the z-scores (along with mean & s.d.) of an array of numbers with scale()
rs <- Cars93$Horsepower[Cars93$Origin == "USA" & Cars93$Cylinders == 8]
scale(rs)

# calculate the ranks of an array of values
rank(rs)

