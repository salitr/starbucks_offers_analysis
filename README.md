# Starbucks: Analyze-a-Coffee

The purpose of the analysis is to examine how Starbucks’ customers respond to an offer whether a BOGO or Discount is the offer. Not all customers have the same incentives to view an offer and then make a transaction to complete the offer. Many factors play an important role in impacting how customers make purchasing decisions; for instance, some customers prefer offers that allow them to collect more and more stars toward getting exclusive perks or even free products. Sometimes, customers at a particular age group, prefer an offer different than what another group prefers. Moreover, we should keep in mind that female customers may react to an offer is different than how male customers do. Many aspects can be investigated and analyzed to find answers to such questions. All of that would help Starbucks to target its customers, and then personalizes and customizes the offers it sends depending on who are the audience.

## Libraries
In addition to importing pandas, numpy, os, matplotlib and multiple sklearn models, all the plots applied in the analysis requires the installation of plotly and cufflinks for interactive plots, and gmaps for mapping.

In case there is an error while importing cufflinks `ModuleNotFoundError: No module named 'cufflinks'`, we need to add the below command in Terminal to download cufflinks. [source](https://medium.com/@hicraigchen/plotly-with-pandas-via-cufflinks-in-jupyter-lab-issues-50fcf1a89a1c)

`pip install git+git://github.com/santosjorge/cufflinks.git#egg=cufflinks -U`

## Motivation
Starbucks possesses a unique way of connecting with and rewarding its customers who purchase its products. Starbucks Rewards program allows the company to create a Loyalty Program where it awards loyal customers by offering incentives for buying products with special offers. It utilizes many channels to market its products from social media to TV spots and ads. Starbucks executes its extraordinary marketing strategy by deploying a combination of marketing media channels, where it creates brand recognition. Starbucks does not only understand its products and customers, but also keeps up with how its customers use technology. Starbucks App enables customers to keep track of the available offers and happy hour deals at participating stores. It allows customers to earn and collect stars (collect two stars per $1) that can be redeemed in-store or via the app.

we are going to investigate and analysis three files that simulate how people make purchasing decisions and how promotional offers influence those decisions. The analysis and its findings are only observational and not the result of a formal study. General business questions are listed below to guide us through the analysis to develop a set of heuristics where the findings are not guaranteed to be optimal or rational. Many questions can be asked; here is some of what we are going to investigate:

1. What is the number of customers who received at least one offer?
2. Who usually spend more at Starbucks, female or male?
3. For the customers who spend more; Who makes more income per year?
4. How old are most of Starbucks customers with respect to gender?
5. How much do customers spend at any time since the start of an offer?
6. Can we find the most popular offer by an age group or a gender, then compare it to other offers, or even another age group?
7. Which offer has made the most for Starbucks? Is there a difference between BOGO offers and Discount offers?
If so, Do male customers react the same as female customers do for any of the two offer types?

## File Descriptions
1. The datasets that we have and we are going to read, clean, and analyze:

  * **portfolio.json** —explanation of each variable in the file:
    - id: offer id
    - offer_type
    - difficulty: minimum required spend to complete an offer
    - reward: stars given for completing an offer
    - duration: time for offer to be open, in days
    - channels
  * **profile.json** —explanation of each variable in the file:
    - age
    - became_member_on: date when customer created an app account
    - gender
    - id: customer id
    - income
  * **transcript.json** —explanation of each variable in the file:
    - event: record description (transaction, offer received, viewed, etc.)
    - person: customer id
    - time: time in hours since start of an offer
    - value: either an offer id or transaction amount depending on the event

2. **starbucks_analyze_a_coffee.ipynb** A copy of the notebook with a complete code cells

## Results
My post in Medium shows the main findings of the analysis.
  * [**Starbucks: Analyze-a-Coffee**](https://medium.com/@salitr/boston-airbnb-analysis-f46bcda1713a)

A summary of the findings:
1. Eight offer (4 BOGO and 4 Discounts) were sent to 14,825 customers who made 26,226 transactions while completing at least one offer.
2. Female customers account for 41.30% and male customers account for 57.20% of the data overall whether they all completed an offer, made a transaction before the end of an offer or not.
3. On average, male customers make less than female customers do in a year. Female customers make more than the average income per year for all gender types. While female customers make on average around 71k a year, male customers make on average around 61k.
4. Most customers of all gender types make between 40k and 60k. Most of the female customers make between 60k and 80k while most male customer make between 40k and 60k a year.
5. On average, female customers are older than male customers. The majority of the customers for both gender are between 40 and 60 years old.
6. On average, all customers paid an overall amount of $16.55 at any time since an offer has started. Female customers paid more than the average at any time! Whereas male customers most the time paid less than the average.
7. Offers 5 and 7 made the most total transaction amounts paid by all customers who completed an offer and made at least one transaction: $194,632 and $149,296.9, respectively. All customers, on average, have responded to and paid more for offer 5 almost always more than what they did for offer 7 at any time.
8. Offer 2 made the highest amount of money among the four BOGO offers with a total of $110113.8 paid by all customers. Female customers paid more than male customers for any of BOGO offers.
9. Offer 5 made the highest amount of money among the four Discount offers. Female customers paid more than male customers for any of Discount offers. Offer 5 is the most popular offer with 82% completion rate.
10. With respect to customers age, offer 5 has the highest completion rate 77.55% by customers who are 25 years old. While customers age 35 or 45 years old prefer offer 6 with a completion rate of 82.61% and 83.33%, respectively.

## Licensing and Acknowledgement
The datasets used in this analysis were provided by Udacity. Also, plotly provides examples of codes for different types of plots of which some have been adapted, edited, and used as needed.
