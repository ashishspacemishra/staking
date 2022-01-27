A platform for yield farming where a user with mDAI tokens can stake his coins to Token Farm and get DAPP tokens as rewards. User can unstake any time to get his mDAI tokens back. The DAPP token rewards are given at regular intervals by owner of farm and its value will depend upon the number of tokens staked 
(for staking 1 mDAI reward = 1 DAPP) 


# prerequistes
install Ganache client: https://trufflesuite.com/ganache/
install yarn

# build & run
npm install
yarn
npm start

# add ganache custom network in Metamask
1. go to Networks > Add a network
  1.a Network Name (Any custom name), New RPC URL (Ganache server network address), Chain ID (any available id)
2. Add Test account. go to Import Account
  2.a Select Type -> Private Key
  2.b paste private key from ganache account
3. Do it for both Account A & B

# deploy smart contract
truffle compile
truffle migrate --reset (to put new snart contract on blockchain)

# tests
truffle test

# process
configurable through script::: 2_deploy_contracts.js
total DAPP token = 1million tokens (Account A) - SC account
total mDAI token = 100 tokens (Account B) - Investor

truffle console

# issue tokens
truffle exec scripts/issue-token.js
