# Churn_EDA_Music_Streaming_Service
 The overall goal of this exploratory data analysis is to build an algorithm for the subscription business that predicts whether a user will churn after their subscription expires based on the analysis of user attributes and behavior on the website.
____________________________________________________________________________________________________________________________________________
### Data Description
The dataset for this ipynb requires all (4) of the following:

    train.csv - the train set, containing the user ids and whether they have churned.
        -msno:  This is the user id
        -is_churn:  This is the target variable. Churn is defined as whether the user did not continue the subscription 
                    within 30 days of expiration. is_churn = 1 means churn,is_churn = 0 means renewal.

    transactions.csv
        -msno:  user id
        -payment_method_id:  payment method
        -payment_plan_days:  length of membership plan in days
        -plan_list_price:  in New Taiwan Dollar (NTD)
        -actual_amount_paid:  in New Taiwan Dollar (NTD)
        -is_auto_renew:  membership auto-renewal option
        -transaction_date:  format %Y%m%d
        -membership_expire_date:  format %Y%m%d
        -is_cancel:  whether or not the user canceled the membership in this transaction.

    user_logs.csv
        -msno:  user id
        -date:  format %Y%m%d
        -num_25:  # of songs played less than 25% of the song length
        -num_50:  # of songs played between 25% to 50% of the song length
        -num_75:  # of songs played between 50% to 75% of of the song length
        -num_985:  # of songs played between 75% to 98.5% of the song length
        -num_100:  # of songs played over 98.5% of the song length
        -num_unq:  # of unique songs played
        -total_secs:  total seconds played

    members.csv
        -msno:  user id
        -city:  user city
        -bd:  age (Note: this column has outlier values ranging from -7000 to 2015, please use your judgement)
        -gender  user gender
        -registered_via:  registration method
        -registration_init_time:  format %Y%m%d

