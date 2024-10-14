# The_CrowdFunding_smart_contract

**Description-**
This Solidity smart contract is designed to facilitate a crowdfunding campaign. The contract allows multiple contributors to donate funds towards a project, with an option to create spending requests that require approval from the contributors. The campaign includes features like minimum contribution requirements, a funding goal, and a deadline.

**Features-**
- *Contribution Tracking:* Keeps track of each contributor's donations.
- *Minimum Contribution:* Enforces a minimum contribution amount.
- *Funding Goal and Deadline:* Sets a target amount to be raised before the deadline.
- *Request Management:* Allows the contract owner to create spending requests for the collected funds.
- *Voting Mechanism:* Contributors can vote to approve or reject spending requests.

**Contract Details-**
1. *State Variables:*
   - contributors: A mapping to track contributions from each address.
   - admin: The address of the campaign administrator.
   - noOfContributors: The number of unique contributors.
   - minimumContribution: The minimum amount required to participate in the crowdfunding.
   - deadline: The campaign end time, specified as a timestamp.
   - goal: The funding target for the campaign.
   - raisedAmount: The total amount of funds raised.

2. *Request Structure:*
   - description: A brief description of the spending request.
   - recipient: The address that will receive the funds if the request is approved.
   - value: The amount requested.
   - completed: A flag to indicate if the request has been fulfilled.
   - noOfVoters: The number of contributors who have voted on the request.

**Functions-**
- *Contribution Functions:*
  - contribute(): Allows users to contribute to the crowdfunding campaign, provided the minimum contribution requirement is met.

- *Admin Functions:*
  - createRequest(): Creates a new spending request.
  - makePayment(): Executes the payment for an approved request.

- *Voting Functions:*
  - voteRequest(): Allows contributors to vote on a spending request.

**Usage-**
1. *Deploy the contract* to a blockchain network (e.g., Ethereum).
2. *Contribute to the campaign* by calling the contribute() function.
3. *Create spending requests* for project expenses if you are the admin.
4. *Vote on spending requests* as a contributor to approve or reject the proposal.
5. *Make payments* for approved requests using the makePayment() function.

**Prerequisites-**
- Solidity version >=0.6.0 <0.9.0.
- Ethereum wallet (e.g., MetaMask) for deploying and interacting with the contract.

**Security Considerations-**
- Only the admin should be allowed to create spending requests.
- The makePayment() function should be protected against reentrancy attacks.


