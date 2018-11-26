# Data-Exploration-in-R--Line-plot-with-customized-line-types-add-abline-in-histogram-scatter-plot-w
Data Science updates:-Data Exploration in R:-Line plot with customized line types, add abline in histogram, scatter plot with different (like Cluster Analysis) categories  
############## Subscribe this YouTube Channel Data/Fun  ####################################################
########## line plot

weeks<-c(1:10)

orders<-c(12,24,34,34,36,37,43,45,48,49)

demand<-data.frame(weeks,orders)

str(demand)

##only points 

plot(demand$weeks,demand$orders,xlab = "Week",ylab = "Order", type = "p") #only points 

##line

plot(demand$weeks,demand$orders,xlab = "Week",ylab = "Order", type = "l") #line

##Both

plot(demand$weeks,demand$orders,xlab = "Week",ylab = "Order", type = "b") #Both 

##stair steps

plot(demand$weeks,demand$orders,xlab = "Week",ylab = "Order", type = "s") # stair steps
############## Subscribe this YouTube Channel Data/Fun  ####################################################
## plot above all plot in one window
par(mfrow=c(2,2))

plot(demand$weeks,demand$orders,xlab = "Week",ylab = "Order",main = "Points" ,type = "p") #only points 

plot(demand$weeks,demand$orders,xlab = "Week",ylab = "Order",main = "Line", type = "l") #line

plot(demand$weeks,demand$orders,xlab = "Week",ylab = "Order",main = "Points & line", type = "b") #Both 

plot(demand$weeks,demand$orders,xlab = "Week",ylab = "Order",main = "steps", type = "s") # stair steps

############## Subscribe this YouTube Channel Data/Fun  ####################################################

## Add line in Histogram on mean and median point
hist(demand$orders,breaks = 4, xlab="orders",main = "Distribution of order",col = "skyblue")

abline(v=mean(orders),col="red",lwd=3,)

abline(v=median(orders),col="green",lwd=3,)

legend("topleft",c("Mean","Median"),pch=c(16,16),col=c("red","green"))

############## Subscribe this YouTube Channel Data/Fun  ####################################################

## Scatter plot for differnt categories  
dim(iris)

head(iris)

levels(iris$Species)

############## Subscribe this YouTube Channel Data/Fun  ####################################################

plot(iris$Sepal.Length,iris$Sepal.Width,xlab = "Sepal length",ylab = "Sepal witdh",main = "Different Species with Sepal length and witdh", type = 'n')

##Subseting by Different Species

setosa<-iris[iris$Species=='setosa',]#subset iris data 

versicolor<-iris[iris$Species=="versicolor",]

virginica<-iris[iris$Species=="virginica",]

## ploting ploins with Different Species

points(setosa$Sepal.Length,setosa$Sepal.Width,pch=8,col="red")

points(versicolor$Sepal.Length,versicolor$Sepal.Width,pch=22,col="blue")

points(virginica$Sepal.Length,virginica$Sepal.Width,pch=11,col="Orange")

## Adding Legend

legend("bottomright",c("setosa","versicolor","virginica"),pch = c(8,22,11),col=c("red","blue","Orange"))

############## Subscribe this YouTube Channel Data/Fun  ####################################################

