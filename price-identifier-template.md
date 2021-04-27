*An UMIP number will be assigned by an editor. When opening a pull request to submit your UMIP, please use an abbreviated title in the filename. The file name should follow this format - "umip_add_priceidentifiername.md". Please remove this and all italicized instructions before submitting your pr. All bolded fields should be filled in before submission.*

## Headers

| UMIP                |                                                               |
| ------------------- | ------------------------------------------------------------- |
| UMIP Title          | Add DIGG Positive Rebases as a supported price identifier     |
| Authors             | Jon (BadgerDAO)                                         |
| Status              | Draft                                                         |
| Created             | 4/27/2021                                             |
| Discourse Link      | **Create a post in [UMA's Discourse](https://discourse.umaproject.org/c/umips/18) and link here**            |

# Summary 

The DVM should support price requests for total DIGG Positive Rebases in a set timeframe. A DIGG Positive Rebase can be determined if the total supply of DIGG (https://etherscan.io/token/0x798d1be841a82a273720ce31c822c61a67a601c3) increased from one day to the next.


# Motivation

We would like this identifier added so that we can distriute positive rebase options as a mechanism to help support the stability of DIGG.  More details on the campaign can be found in this post:
https://medium.com/badgerdao/badgerdao-x-uma-introducing-rebase-mining-3c663a5abdce

# Data Specifications

-----------------------------------------
- Price identifier name: **Rebase_Pos_DIGG_30d_Jun0721** 
- Markets & Pairs: **N/A**
- Example data providers: **Available on-chain** 
- Cost to use: **None**
- Real-time data update frequency: **Daily** 
- Historical data update frequency: **Daily** 

# Price Feed Implementation

At 12:00 UTC every day compare the total supply of DIGG (https://etherscan.io/token/0x798d1be841a82a273720ce31c822c61a67a601c3) to its supply from the previous day.  If it is greater than the previous day then the price feed should iterate by 1.  For the purpose of this version of the opions the possible values for this price feed to return at the time of maturity will be between 0 and 30

# Technical Specifications



# Rationale

I think comparing total supply one day to the other is the easiest but am open to other ways to implement this.

# Implementation

*Describe how UMA tokenholders should arrive at the price in the case of a DVM price request. Document each step a voter should take to query for and return a price at a specific timestamp. This should include an example calculation where you pick a specific timestamp and calculate the price at that timestamp.*

# Security Considerations

None
