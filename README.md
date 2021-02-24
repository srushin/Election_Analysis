# Election_Analysis

## Project Overview
A Colorado Board of Elections employee has given the following tasks to complete the election audit of a recent local congressional election.

1.	Calculate the total number of votes cast.
2.	Get a complete list of candidates who received votes.
3.	Calculate the total number of votes each candidate received.
4.	Calculate the percentage of votes each candidate won.
5.	Determine the winner of the election based on the popular vote. 

## Resources
-	Data Source: election_results.csv
-	Software: Python 3.6.1, Visual Studio 1.38.1

## Summary
The analysis of the election show that:
-	There were 369,711 votes cast in this election
-	The candidates were:
    - Charles Casper Stockham
    - Diana DeGette
    - Raymon Anthony Doane

-	The candidate results were:
    - Charles Casper Stockham received 23.0% of the votes and 85,213 number of votes.
    - Diana DeGette received 73.8% of the votes and 272,892 number of votes.
    - Raymon Anthony Doane received 3.1% of votes and 11,606 number of votes.

-	The winner of the election was:
    - Diana DeGette, who received 73.8% of the votes and 272,892 number of votes.

## Challenge Overview
The Colorado Board of Elections has asked to expand on the original tasks of the election audit. Using the same election_results.csv, they are now looking to include:
- The voter turnout for each county
- The percentage of votes from each county out of the total count
- The county with the highest turnout

All of the above tasks are to be printed on the command line as well as written to a text file. 

## Challenge Election-Audit Results
The election- audit challenge results show that
- Jefferson County cast 38,855 votes which was 10.5% of the total votes for the precinct.
- Denver County cast 306,055 votes which was 82.8% of the total votes for the precinct.
    - Denver County cast the most votes this election with 306,055.
- Arapahoe County cast 24,801 votes which was 6.7% of the total votes for the precinct.

>These vote numbers were tabulated using by using an `if` statement to lookthrough csv, add the name of the county to an empty list, then index it within an empty dictionary. I initalized the dictionary key value to 0 and began adding to that total by 1 for every apparence of the county name.  
>![county_vote_counting](https://user-images.githubusercontent.com/78064648/109051199-20f10780-768f-11eb-91e7-258a1dac2f76.png)
>Next I used a `for` loop to `.get` the values in the dictionary for each county, calculate the percentage of the total votes and print/write the results to the command line and text file respectively. This was followed by an `if` statement within the `for` loop to determine the county with the largest voter turnourt. Again, this was printed/written to the aforementioned command line and text file.
>![county_percent_print](https://user-images.githubusercontent.com/78064648/109051207-22223480-768f-11eb-9478-8a547edd8f58.png)

## Challenge Summary
This script is a straight forward way of looking over large amounts of voter data information to determine the outcome or to audit an election. It is quick, efficient, and can be taylored to any type of election. A few areas that can be altered to serve different or larger elections can be the inclussion of a `for` & `if` statement that verifies there are not any duplicate Ballot ID numbers. If there is a duplicate number, the duplicate row can be removed or ignored from the counting process. This would ensure that there are not multiple counts of the same ballot. This script can also be altered to accomidate a ranked choice election, like Maine and New York have. Similar to the way this runs now, each candidates votes would be tabulated, the totals would go through an `if` statment to determine if any candidate recieved more than 50% of the vote. If they did, the highest vote geter wins the election, if not, then the lowest candidate is dropped. Those voters second choice would be tabulated with a `for` loop to determine the winner. This can be expanded to as many candidates as necessary. 

