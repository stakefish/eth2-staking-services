# Ethereum 2.0 Staking Services List
This repo is used as main database for the Ethereum 2.0 Staking Services List that you can find here: https://stake.fish/en/ethereum/services/

## Updating the list

If you want to add a new staking service to the list, or if you think something is not correct, you can submit a pull request to [this file](https://github.com/stakefish/eth2-staking-services/blob/main/eth2-staking-services.json) with the desired modifications. 

Please use the following JSON structure

```json
{
    "name": "Your name",
    "website": "https://your.website",
    "type": "non-custodial",
    "stake": "32 ETH",
    "fee": "$5",
    "feeType": "MONTHLY_PAYMENT",
    "networks": 4,
    "location": "United States",
    "socials": [
      {
        "name": "telegram",
        "url": "https://t.me/yourgroup"
      },
      {
        "name": "twitter",
        "url": "https://twitter.com/yourhandle"
      },
      {
        "name": "discord",
        "url": "https://your.discord"
      }
    ]
},
```

### Fields description

| Field | Description | Required |  
|-------|-------------|----------|
|name|The name of the service|Yes| 
|website|URL of the website (https)|No|  
|type|can be **custodial**, **non-custodial** or **?**|Yes|
|stake|The minimum amount required to stake|Yes|
|fee|Fee amount|Yes|
|feeType|Can be: **UNKNOWN**, **MONTHLY_PAYMENT**, **REWARDS_PERCENTAGE** or **ONE_TIME_PER_VAL**|Yes|
|networks|How many other networks the service supports|Yes|
|location|Country of the service|No|
|socials|Array of name+url of every social of the service|No|

Type can be **?** when custody of keys is not very clear, for example in the case of pools. If you have another kind of fee, please write as comment in the Pull Request and we will add support for it.




