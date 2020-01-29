library(tidyverse)
raw_data <- read.csv("311-service-request.csv")
restricted_data <- read.csv("restricted.csv")

area_data <- filter(raw_data, raw_data$Incident.Zip >= 10025
                    & raw_data$Incident.Zip <= 10027)

Years <- format(as.Date(area_data$Closed.Date,"%m/%d/%Y"), format = "%Y")
area_data$Years <- Years

simDara <- data.frame("Created.Data" = area_data$Created.Date, 
                      "Latitude" = area_data$Latitude,
                      "Longtitude" = area_data$Longitude,
                      "Years" = area_data$Years) 

smol_data <- data.frame("Created.Date" = restricted_data$Created.Date,
                        "Closed.Data" = restricted_data$Closed.Date,
                        "Latitude" = restricted_data$Latitude........,
                        "Longtitude" = restricted_data$Longitude...All)

smol_data$Created.Date <- format(as.Date(smol_data$Created.Date,"%m/%d/%Y"), 
                                 format = "%Y-%m-%d") 
smol_data$Closed.Data <- format(as.Date(smol_data$Closed.Data,"%m/%d/%Y"), 
                                 format = "%Y-%m-%d")


write.csv(simDara,'coordData.csv')

d10 <- filter(simDara, simDara$Years == 2010)
d11 <- filter(simDara, simDara$Years == 2011)
d12 <- filter(simDara, simDara$Years == 2012)
d13 <- filter(simDara, simDara$Years == 2013)
d14 <- filter(simDara, simDara$Years == 2014)
d15 <- filter(simDara, simDara$Years == 2015)
d16 <- filter(simDara, simDara$Years == 2016)
d17 <- filter(simDara, simDara$Years == 2017)
d18 <- filter(simDara, simDara$Years == 2018)
d19 <- filter(simDara, simDara$Years == 2019)
d20 <- filter(simDara, simDara$Years == 2020)

write.csv(d10,'d10.csv')
write.csv(d11,'d11.csv')
write.csv(d12,'d12.csv')
write.csv(d13,'d13.csv')
write.csv(d14,'d14.csv')
write.csv(d15,'d15.csv')
write.csv(d16,'d16.csv')
write.csv(d17,'d17.csv')
write.csv(d18,'d18.csv')
write.csv(d19,'d19.csv')
write.csv(d20,'d20.csv')

p <- ggplot(area_data, aes(x = area_data$Longitude, y = area_data$Latitude))


p + geom_point(aes(color = Years), alpha = 0.6) + 
  scale_x_continuous(limits = c(-73.98, -73.93)) +
  scale_y_continuous(limits = c(40.78, 40.83)) +
  facet_wrap(~Years)

ggplot(area_data, aes(x = area_data$Years)) + geom_bar()

