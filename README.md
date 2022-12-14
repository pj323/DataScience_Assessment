# Data_Science_test_Ping_Tree

Bidding Assessment
Preetham John


I have not used any model but instead i have set rules and tested it against the rules This is my Approach and a detailed explanation for the same.

The code is completely written in ipynb (pyhton Notebooks).
Before running the 11th cell we must run the 26th cell cause df_accepetd is defined in that cell.


The data was entered into a Python-written Jupyter Notebook to start the task. The data types were discovered to be what was anticipated, and the data missingness was discovered to be totally contained in the BidPrice column, reflecting cases that were not put up for bid. The bid prices were verified to match the predicted price points. The ID 59826378 was discovered to be duplicated. Given that the values in each row of the id instance matched, it was concluded that this row was a duplication. This is how I decided to eliminate one of the duplicate rows from the data. After that, I added another row to the data that would represent the anticipated payout for each bid instance. 

A preliminary study of the data presented revealed that some bids had been made in situations where the predicted return amounts were significantly less than the bid price. These bids resulted in a $1055.02 net loss. In the future, it will be crucial to make sure that only chances with a projected return greater than the bid cost are targeted for bids.

I examined the estimated revenue, expected conversion, and expected return distributions of the approved and rejected bids to further analyze the data. The bids in the 75 accepted bids group contributed 55.6 percent of the total expected net return, the accepted bids at 35 contributed 37.3 percent, the accepted bids at 50 contributed 4.1 percent, and the accepted bids at 3 contributed 3 percent.

When I analyzed samples of accepted and rejected predicted revenue distributions at each bid price using t-tests with an alpha level set at.05, I discovered that there was no significant difference between the distributions at the 75 bid price. The remaining distributions of predicted income that were approved and rejected at 50, 35, and 3 were, nonetheless, statistically distinct, in my opinion. The results of statistical significance at each bid price are consistent with the results of the expected revenue distributions when t-tests at the.05 level are used to compare expected conversion distributions at each bid price.

Analysis of the expected return distributions revealed that the 75 group sample, with a p-value of.0564, slightly missed statistical significance. However, it has been determined that the distribution at 50 is statistically distinct. Furthermore, it was discovered that the predicted return distributions at 35 and 3 were not statistically distinguishable. When deciding which distribution groups can fairly be expected to react to modifications to the bidding model, comparing the statistical significance of these distribution sets provides useful information.

Calculating the anticipated net return per bid using the provided example rules was the first step in investigating potential changes to the bidding model. With 21916 total bids put, the projected return per bid based on the example rule set returns as 59.70 dollars. I developed a procedure to raise these expected return criteria based on the calculated expected return for each bid price. Through numerous iterations, it was discovered that the 35 and 50 projected revenue thresholds converged to 650 dollars. I then ran a test to see if dropping the 35 price point had a negative impact on the anticipated net return per bid. I decided to eliminate the bid price because the calculations showed that doing so had no impact on the anticipated net return. As a result, the final model criteria are as follows: if the predicted return is larger than $690, apply the $75 bid; if it is greater than 650, apply the $50 bid; and, finally, apply the $3 bid when it is greater than $64, apply the 3 dollar bid. For a total of 15,318 bids, this setup yields an expected net return per bid of 133.12 dollars.

To sum up, if I were to pursue this topic further, I would like to develop a model that would help predict if a proposed bid would be accepted based on prior market experience. I believe that such a resource would offer a fantastic opportunity for testing with various predicted revenue threshold configurations.
