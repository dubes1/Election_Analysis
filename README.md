# Election_Analysis  

## Project Overview  
A Colorado Board of Elections has given you the following tasks to complete the election audit of a recent local congressional election.  

1. Calculate the total number of votes cast.  
2. Get a complete list of candidates who received votes.  
3. Calculate the total number of votes each candidate received.  
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on the popular vote.  
6. Calculate the total number of votes were cast in each county
7. Calculate the the percentage of votes were cast in each count
8. Determine the county with the highest turnout

## Resources  
- Data Source: [election_results.csv](https://github.com/dubes1/Election_Analysis/files/7079036/election_results.csv)
- Software: Python 3.6.1, Visual Studio Code, 1.38.1  

## Results  
The Results of the election show that:  
- There were 369,711 votes cast in the election.  
- The candidates were:  
  - Charles Casper Stockham
  - Diana DeGette
  - Anthony Doane  
- The candidate results were:  
  - Charles Casper Stockham received 23.0% of the vote and 85,213 votes.  
  - Diana DeGette received 73.8% of the vote and 272,892 votes.  
  - Anthony Doane received 3.1% of the vote and 11,606 votes.  
- The winner of the election was:  
  - Diana DeGette, who received 73.8% of the vote and 272,892 votes.
- The counties that cast votes were
  - Jefferson
  - Denver
  - Arapahoe
- The county results were:
  - Denver cast 82.8% of all votes with 306,055 votes cast
  - Jefferson cast 10.5% of all votes with 38,855 votes cast
  - Arapahoe cast 6.7% of all votes with 24,801 votes cast
- The county with the highest amount of votes cast was Denver with 82.8% of all votes cast (306,055 votes cast)  

## Election-Audit Summary  
This script can be used for any election if you modify the script to account for geographic zone instead of county based on the type of election that it is. Another modification could be to account for a run off election where if no candidate gets 50% of the vote there is no declared winner and the top 2 candidates go to a run off election. Modifying the first change would be on the  
if (votes>Countywinning_count) and (Countyvote_percentage>winning_percentage):  
         Countywinning_count = votes  
         winning_county = county_name  
         Countywinning_percentage = Countyvote_percentage  
         winning_county_summary = (  
        f"-------------------------\n"  
        f"Largest County Turnout: {winning_county}\n"  
        f"-------------------------\n")  
formula changing the county name to whatever geographic area the vote is done in  
modifying the run off code would be adding an if statement before this snippet of code in line 157  
if (votes > winning_count) and (vote_percentage > winning_percentage):  
            winning_count = votes  
            winning_candidate = candidate_name  
            winning_percentage = vote_percentage  
adding if (votes > winning_count) and (vote_percentage > winning_percentage): and (winning_percentage > .5)  
then take the top 2 and put them in a run-off election
