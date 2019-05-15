####
# VIX import
####

library(rvest)
library(dplyr)

getwd()
setwd("if needed")

# save url's
#http://www.cboe.com/products/vix-index-volatility/vix-options-and-futures/vix-index/vix-historical-data
hist.url <- read_html("http://www.cboe.com/products/vix-index-volatility/vix-options-and-futures/vix-index/vix-historical-data")

# scrape tables from url into a list
hist_tbls <- scrapetbls(hist.url)

# hist1.tbls <-hist.url %>%
#   # gets all tables 
#   html_nodes(".icon-css-arrows li a") %>%
#   html_name()
# rm(hist1.tbls)


# for (i in seq_along(vix.tbls)) {
#   tbl.name <- paste("vix.tbl",i,sep=".")
#   x <- as.data.frame(vix.tbls[[i]])
#   assign(tbl.name,x)
# }
# rm(x)


###

setwd('F:/R Projects/VIX/Tables')
# creates list of TXT files assuming they are in the working dir
csvfiles <- as.list(list.files(pattern = '*.csv'))
csvfiles
for (i in csvfiles) {
  x <- read.delim(i, header=TRUE, sep=",",na.strings = "NA")
  assign(i,x)
    rm(x)
  }
 


