# Money Funding & Laundering Bots for Aztec Protocol

## Intro

Most attacks begin and end with the use of private services that allow funding or withdrawals without revealing the
sender and recipient.

The most popular service among attackers of DeFi projects was the [Tornado Cash](https://twitter.com/tornadocash) mixer.
However, after it was blocked by The US Department of Treasury, other projects will likely take over this niche. 
[Aztec Protocol](https://aztec.network/), which is a privacy-first zk-rollup on Ethereum, could be a potential such project.

<img alt="Money Funding & Laundering Bots for Aztec Protocol" src="./blob/preview.png"  height="290">

## Status

> The proposal was created on Gitcoin

## The Proposal

To improve attack detection in the [Forta Protocol](https://forta.org/) ecosystem, it is proposed to develop two separate bots covering both
the account funding stage before an attack and the money laundering stage that occurs after the attack is performed.

### Funded Account Interaction Bot

This bot detects when an account that was funded by Aztec Connect interacts with a contract.
The severity of these findings is low, as they do not indicate malicious activity. However, in the presence of other
suspicious activity, they greatly increase the accuracy of attack detection.

### Money Laundering Bot

This bot detects when numerous large transfers are made to Aztec Connect, potentially indicating post-hacking money
laundering activity. All user transfers are summed up within a specified time and checked for exceeding the threshold.
The severity of such findings is high.

These bots will work similarly to existing bots for Tornado Cash, and I'm sure they will be able to increase the
accuracy as well as the number of detected attacks. 
