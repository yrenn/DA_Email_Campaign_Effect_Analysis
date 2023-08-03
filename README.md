# DA_Email_Campaign_Effect_Analysis

The case analyses the different impacts of email campaigns. Firstly, we divide customers into a control group and a target group and send Email campaigns to different groups. Through the analysis of the following parameters using SQL, get the best Email campaign. The parameters are as follows:

1. conversation rate: PurchasedClient# / totalClient#
2. unsubscribe rate: UnsubscribeClient# / totalClient#
3. open rate: 'open_email'actionClient# / totalClient#
4. click rate: 'click_content'actionClient# / totalClient#
5. Daily Average Revenue per active client: By per transaction date level, sum(txamount)/activeClient#
6. Daily Average Revenue per contributed client: By per transaction date level, sum(txamount)/transactionClient#
7. Day 10/30 retention rate:  transactionClient# in recent 10/30 days and last period/ TotalClient# in last period
8. churn rate: transactionClient# in last period but no in this period/ TotalClient# in last period
9. % rate lift between control and target group: (TotalTransactionAmount in target group - TotalTransactionAmount in the control group)/TotalTransactionAmount in the control group
10. CLV: Customer Lifetime Value: assess the total value a customer brings to a business over their entire relationship. 

## Data model
The graph shows the Snowflake Schema of the data model

![email_campaign](https://github.com/yrenn/email_campaign/assets/118937529/d61c71a9-dfca-48cb-865f-29d0562f393b)

# lesson learned
1. There are some important parameters such as retention rate and churn rate to assess the short-term and long-term effectiveness of each email campaign.
2. We use A/B test and rate lift to assess if each email campaign performs well.
3. Determine the required indicators and specific requirements with other departments when specifying indicators. For example, we use 10 days as a short term and 30 days as a long term when we calculate the retention rate.


