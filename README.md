Traditional financial markets have little room for creative approaches. When market participants transact, buyer and sellers must meet at a common price. 
Without getting too technical, institutions give retail traders the ability to transact instantly by charging them premiums in the form of bid/ask spreads,
a built in fee that is nearly impossible to overcome for frequent traders.
<br/>
<br/>
This platform gives users an interface to track real asset prices and make buy/sell transaction "on paper". This removes the need to cross the spread,
as well as any other regulations related to change in ownership of assets. This system does not allow for the traditional methods of capturing a profit, since
no asset is being bought or sold. Instead, the performance of the user is tracked by the platform and they are placed on a leaderboard. 
Currently there are two leaderboards, one with risk and one without risk. Users start on the riskless leaderboard, where only the interest generated by the 
prize pool gets redistributed. Then, top performers on the riskless leaderboard get access to the leaderboard where the entire prize pool is redistributed. 
<br/>
<br/>
The current system for redistribution works like this:
Users buy into the competition with a minimum deposit of 50 usd. At the end of the competition, top 10% recieve bottom 90%. Starting with 1st place, and 
descending towards the last user in the tp 10%, we calculate the user's deposit relative to the deposits of all users below them in the top 10%. We award them
their relative share of the winnings. Then increment to the next user and repeat with the remaining funds. To clarify, when calculating the rewards of the 
second user, we do not take into account the first user anymore. We look at the deposit of the second user relative to the deposits of all user below the second
user who placed in the top 10%, and then award the proportional amount of the remaining prize pool. 
<br/>
<br/>
Deposits should be made to a public ethereum contract in a stable coin (tbd). Contract checks that the user is depositing min of 50 usd and that user has not 
yet made a deposit for this season. Then stores user address and funds deposited. The rest depends on the efficiency of the blockchain we choose... either 
an authorized wallet will change the state of the winners variable at the end of the season, at which point the profits will be redistributed to those in 
the list, and the contract will reset (the protocol itself keeps a percent). This makes for minimum blockchain transactions and minimum gas fees. 
The ideal alternative is for all buy/sell transactions to be logged on the blockchain, and for the leaderboard to be calculated on the blockchain based on the 
transaction log of the users. This makes everything public and automated, but requires many transactions to be made. On the other hand, updating a single
variable may be insignificant on some chains. 
