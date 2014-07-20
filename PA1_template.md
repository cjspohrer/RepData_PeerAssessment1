# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data

```r
unzip("activity.zip")
activity <- read.csv("activity.csv")
```

## What is mean total number of steps taken per day?
1. Make a histogram of the total number of steps taken each day


```r
daily.steps <- aggregate(steps ~ date, data=activty, FUN=sum)
```

```
## Error: object 'activty' not found
```

```r
barplot(daily.steps$steps, names.arg=daily.steps$date, xlab="data", ylab="steps")
```

```
## Error: object 'daily.steps' not found
```

2. Calculate and report the **mean** and **median** total number of steps taken per day


```r
mean(daily.steps$steps)
```

```
## Error: object 'daily.steps' not found
```

```r
median(daily.steps$steps)
```

```
## Error: object 'daily.steps' not found
```

## What is the average daily activity pattern?
1. Make a time series plot (i.e. `type = "l"`) of the 5-minute
   interval (x-axis) and the average number of steps taken, averaged
   across all days (y-axis)


```r
interval.steps <- aggregate(steps ~ interval, data=activty, FUN=mean)
```

```
## Error: object 'activty' not found
```

```r
plot(interval, type="1")
```

```
## Error: object 'interval' not found
```

2. Which 5-minute interval, on average across all the days in the
   dataset, contains the maximum number of steps?


```r
interval.steps$interval[which.max(interval.steps$steps)]
```

```
## Error: object 'interval.steps' not found
```


## Imputing missing values
1. Calculate and report the total number of missing values in the
   dataset (i.e. the total number of rows with `NA`s)


```r
sum(is.na(activity))
```

```
## [1] 2304
```

2. Devise a strategy for filling in all of the missing values in the
   dataset. The strategy does not need to be sophisticated. For
   example, you could use the mean/median for that day, or the mean
   for that 5-minute interval, etc. 

3. Create a new dataset that is equal to the original dataset but with
   the missing data filled in.
   






