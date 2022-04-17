# Sinking Fund Tracker

## Description
A basic Rails App to track transactions into and out of Sinking Funds. 

### Planned Features
- Ability to view status of funds vs their target amount
- Ability to CRUD Sinking Fund and Transactions
- Ability to set up and automatically add credits to funds (e.g. mimicking add a direct debit)
- 
### Model Design
Two main models are needed:
1. SinkingFund model
Field Name | Type | Description
name | String | Name of sinking fund
target_amount_in_cents | Integer | Target amount of the Sinking Fund (can be either general target like an Emergency Fund or a specific purchase amount e.g. Amazon Prime membership fee)
deadline | Date | Optional - if a deadline is available for when the fund is needed

2. Transaction Model
Field Name | Type | Description
transaction_at | Date | When transaction occured to/from the fund
type | String | One of Credit (payment into fund) or Debit (spending from fund)
amount_in_cents | Integer | Transaction amount in cents


## TODO
- [x] Create Rails App
- [ ] Create Basic Deployment 
- [ ] Add `SinkingFund` Model
- [ ] Add `Transaction` Model
- [ ] Create Front End for Basic `SinkingFund` Views (e.g. index, new, show, edit)
- [ ] Create Front End for Basic `Transaction` Views (Credit and Debit)

Further Enhancement
- [ ] Create `RecurringTransaction` Model
- [ ] Create Job to add `RecurringPayment` `Payment`s
