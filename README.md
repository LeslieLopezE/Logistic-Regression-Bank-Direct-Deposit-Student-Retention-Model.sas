## Logistic Regression: Bank Direct Deposit and Student Retention Model

### Case: Bank Direct Deposit

Community Bank would like to increase the number of customers who use payroll
deposit. Management is considering a new sales campaign that will require each branch
manager to call each customer who does not currently use payroll direct deposit. As an
incentive to sign up for payroll direct deposit, each customer contacted will be offered
free checking for two years. Because of the time and cost associated with the new
campaign, management would like to focus their efforts on customers who have the
highest probability of signing up for payroll direct deposit. Management believes that the
average monthly balance in a customer’s checking account may be useful predictor of
whether the customer will sign up for direct payroll deposit.

To investigate the relationship between these two variables, Community Bank tried the new campaign
using a sample of 50 checking account customers who do not currently use payroll
direct deposit. The sample data show the average monthly checking account balance
(in hundreds of dollars) and whether the customer contacted signed up for payroll direct
deposit (coded 1 if the customer signed up for payroll direct deposit and 0 if not). The
data are contained in the data set named Bank. xlsx

In this exercise, the following tasks are performed:

a. Writing the logistic regression equation relating x and y for the Community Bank data, use SAS to compute the estimated logistic regression equation:

From Figure 1 in chart "Analysis of maximum likehood estimates" the logistic regresion would be:

p(direct|balance) = (e^(-2.6333 +  0.2202*balance)) / 1+ (e^(-2.6333 +  0.2202*balance))


b. Estimating the probability that customers with an average monthly balance of $1000 will sign up for direct payroll deposit. 

First:
e^(-2.6333 +  0.2202*balance) = e^(-2.6333 +  0.2202*$1000) = e^(217.567) 

Then:
p(direct|balance) = e^(217.567) / (1+ e^(217.567))
p(direct|balance) = 1X10^(-94) = 0


c. Calculating the average monthly balance required to achieve 0.5 probability, supposing Community Bank only wants to contact customers who have a 0.50 or higher probability of signing up for direct payroll deposit. 

p(direct|balance) = e^(-2.6333 +  0.2202*balance) / (1+ e^(-2.6333 +  0.2202*balance)) = 0.5
                                                         e^(-2.6333 +  0.2202*balance) = 0.5 * (1+ e^(-2.6333 +  0.2202*balance))
                                                     0.5 e^(-2.6333 +  0.2202*balance) = 0.5
                                                         e^(-2.6333 +  0.2202*balance) = 1
                                                     ln(e^(-2.6333 +  0.2202*balance)) = ln 1
                                                             -2.6333 +  0.2202*balance = 0 
                                                                               balance = 2.6333 / 0.2202
                                                                               balance = 11.9587
                                       
d. What is the estimated odds ratio? What is the interpretation?


### Case: Student Retention Model

Over the past few years the percentage of students who leave Lakeland College at the
end of the first year has increased. Last year Lakeland started a voluntary one-week
orientation program to help first-year students adjust to campus life. If Lakeland is able
to show that the orientation program has a positive effect on retention, they will consider
making the program a requirement for all first-year students. Lakeland’s administration
also suspects that students with lower GPAs have a higher probability of leaving
Lakeland at the end of the first year. In order to investigate the relation of these
variables to retention, Lakeland selected a random sample of 100 students from last
year’s entering class. The data are contained in the data set named Lakeland.

y=1 if the student returned to Lakeland and y=0 if not

x1= 0, if the student did not attend the orientation program

x2 =1, if the student attended the orientation program

In this exercise, the following tasks are performed:

a. Write the logistic regression equation relating 𝑥!and 𝑥" to y.

b. What is the interpretation of 𝐸(𝑦) when 𝑥" = 0? 

c. For the Lakeland data, use SAS to compute the estimated logistic regression
equation. 

d. Use the estimated logit computed in c) to estimate the probability that students
with a 2.5 grade point average who did not attend the orientation program will
return to Lakeland for their sophomore year. What is the estimated probability for
students with a 2.5 grade point average who attended the orientation program?

e. What is the estimated odds ratio for the orientation program? Interpret it. 

f. Would you recommend making the orientation program a required activity? Why
or why not? 
