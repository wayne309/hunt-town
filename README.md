# Hunt Town
Hunt Town is a web3 builders' guild where builders come together to contribute to the expansion of web3 culture and products.

## 📄 Contracts
- Building.sol: A NFT with ERC721 interface, that can only be minted by locking-up 1,000 HUNT tokens on the TownHall contract for 1 year.
  - Locked-up tokens are returned when the NFT gets burned after the lock-up period
  - Building NFT is a membership pass required to enter the Hunt Town Discord group
  - Members with verified Building NFTs will receive BUILD points in the Hunt Town Discord group everyday
- TownHall.sol: A front facing contract that mints / burns Building NFTs.

## 🧪 Test
```bash
npx hardhat test
```

## ⚙️ Deploy
```bash
npx hardhat run scripts/deploy.js
```

## ⛽️ Gas Consumption
```
·---------------------------------------|---------------------------|---------------|-----------------------------·
|         Solc version: 0.8.17          ·  Optimizer enabled: true  ·  Runs: 20000  ·  Block limit: 30000000 gas  │
········································|···························|···············|······························
|  Methods                              ·                20 gwei/gas                ·       1186.28 usd/eth       │
··················|·····················|·············|·············|···············|···············|··············
|  Contract       ·  Method             ·  Min        ·  Max        ·  Avg          ·  # calls      ·  usd (avg)  │
··················|·····················|·············|·············|···············|···············|··············
|  Building       ·  approve            ·      48607  ·      48619  ·        48613  ·            2  ·       1.15  │
··················|·····················|·············|·············|···············|···············|··············
|  Building       ·  burn               ·      45739  ·      50148  ·        46621  ·            5  ·       1.11  │
··················|·····················|·············|·············|···············|···············|··············
|  Building       ·  safeMint           ·     124795  ·     152795  ·       126662  ·           15  ·       3.01  │
··················|·····················|·············|·············|···············|···············|··············
|  Building       ·  transferFrom       ·          -  ·          -  ·        65265  ·            2  ·       1.55  │
··················|·····················|·············|·············|···············|···············|··············
|  Building       ·  transferOwnership  ·          -  ·          -  ·        28593  ·            1  ·       0.68  │
··················|·····················|·············|·············|···············|···············|··············
|  HuntTokenMock  ·  approve            ·          -  ·          -  ·        46248  ·           15  ·       1.10  │
··················|·····················|·············|·············|···············|···············|··············
|  HuntTokenMock  ·  transfer           ·          -  ·          -  ·        51495  ·           17  ·       1.22  │
··················|·····················|·············|·············|···············|···············|··············
|  TownHall       ·  burn               ·      68866  ·      86956  ·        71881  ·            6  ·       1.71  │
··················|·····················|·············|·············|···············|···············|··············
|  TownHall       ·  mint               ·     192241  ·     208241  ·       194908  ·           18  ·       4.62  │
··················|·····················|·············|·············|···············|···············|··············
|  Deployments                          ·                                           ·  % of limit   ·             │
········································|·············|·············|···············|···············|··············
|  Building                             ·          -  ·          -  ·      2174901  ·        7.2 %  ·      51.60  │
········································|·············|·············|···············|···············|··············
|  HuntTokenMock                        ·          -  ·          -  ·      1140679  ·        3.8 %  ·      27.06  │
········································|·············|·············|···············|···············|··············
|  TownHall                             ·          -  ·          -  ·       664226  ·        2.2 %  ·      15.76  │
·---------------------------------------|-------------|-------------|---------------|---------------|-------------·
```
