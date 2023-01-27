# Outspot: Send-time optimisation


Outspot is an e-commerce flashdeal webshop that does a lot of its marketing by sending emails to our loyal newsletter subscribers. We used to send our emails at certain times in the day. We had 2 time slots where we send our mails, one starts sending emails from 06:00 to 09:00 and another slot sends mails from 12:00 to 15:00.


In `data.csv` you will find some open data of 1000 of our users. It is structured in 2 columns giving the `user_id` and `opened` representing the times a user has opened the mails.


### Example input
| user_id  | opened                         |
|----------|--------------------------------|
| 74819875 | 2022-03-18 15:28:01.000000 UTC |
| 69387793 | 2022-04-19 14:53:03.000000 UTC |
| 74819875 | 2022-06-28 07:03:20.000000 UTC |
| ...      | ...                            |


Provide a python script that based on the data provided gives some info for each user, you can choose one of the following that suits you best or solve both problems, but that is optional:

- The top 3 best send-times of the week for the user.
- A prediction for the next time the user will open an email. given the data is extracted at *26/01/2023* predict when the next open of the user was after this date.


*note: we know that for a predictive model / neural network this is a very small dataset but you can assume we have millions of opens (because we do). For the exercises the method is more important than the result, so you can really show off what level of expertise you have even if it is overkill for this use case / data size.*


Analyze the data and perform a cohort analysis on the data. Analyze the retention rate over the months for new users each quarter (first open that quarter). You can use any tool for this.


## Questions


### What other things could we do to optimize our mailing?


### What is the problem that we may have here because we base our data on the historic data that sends mails at these fixed times, and how can we fix this?


### What would have been great data to add to your cohort analysis and why?


## Deliverables


Deliver a csv `results.csv` with the results in the following columns
`user_id`, `day_1`, `time_1`, `day_2`, `time_2` , `day_3`, `time_3`, `next_open`
weekdays being monday, tuesday, ... and time being in the `hh:mm` format and next_open in the format `YYYY-MM-DD hh:mm`.
If you did one of the 2 leave the rest blank.


## Example output
| user_id  | day_1    | time_1 | day_2  | time_2 | day_3    | time_3 | next_open        |
|----------|----------|--------|--------|--------|----------|--------|------------------|
| 74819875 | monday   | 12:32  | monday | 11:11  | tuesday  | 21:05  | 2023-01-27 14:21 |
| 69387793 | thursday | 08:26  | monday | 14:56  | thursday | 16:32  | 2023-02-25 11:21 |
| 71602891 | saturday | 09:58  | sunday | 09:09  | monday   | 18:23  | 2023-12-25 15:56 |
| ...      | ...      | ...    | ...    | ...    | ...      | ...    | ...              |


For the analysis provide some explanation how you have made the analysis and the files used e.g. python/R/excel/... provide an image of a visualization of the analysis and write down your conclusions.
Provide all your code/excels/... that you used for all exercises preferably through github or a zip.


### Good Luck!
