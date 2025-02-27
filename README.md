## Monad Testnet

Welcome to Monad Testnet, this script will help you to be well positioned for future Testnet launch implementing multi Faucet claim,
Testnet Apps Interactions, Protocols, Contract Deployment, etc... All possible stuff related to Monad

``` bash

MonadTestnet/
├── actions/
│   ├── deploy_contract/
│   │   ├── index.js                  # Main script to compile and deploy simple contracts on testnet
│   │   ├── contracts.sol             # Solidity contracts (up to 10 simple contracts)
│   │   ├── ABI.js                    # Exports only the ABI for a sample contract
│   │   ├── launch.js                 # Deployment script for tokens; prompts for token parameters
│   │   └── NFTs/
│   │       ├── deploy.js             # Interactive NFT deployment script (prompts for collection name, ticket, and max supply)
│   │       └── nft.sol               # NFT contract implementing basic functions (mint, burn, transfer, etc.)
│   ├── StakeStone/
│   │   ├── index.js                  # StakeStone module main script (to be implemented)
│   │   └── ABI.js                    # ABI definitions for StakeStone contracts (to be implemented)
│   ├── Multipli/
│   │   ├── index.js                  # Multipli module main script (handles token claims and asset staking)
│   │   └── ABI.js                    # ABI definitions for Multipli contracts (to be implemented)
│   ├── Ambient-Finance/
│   │   ├── index.js                  # Main script for Ambient-Finance module (to be implemented)
│   │   └── ABI.js                    # ABI definitions for Ambient-Finance contracts (to be implemented)
│   ├── Apriori/
│   │   ├── index.js                  # Main script for stake_apr.io module (handles staking & APR token operations)
│   │   ├── ABI.js                    # ABI definitions for Apriori contracts (implemented)
│   │   ├── faucet.js                 # Faucet script for Apriori (to be implemented)
│   │   └── scripts/                  # Additional scripts for Apriori (empty for now)
│   ├── NFTs-Mint/                    # Module for minting NFTs
│   │   ├── MagicEden/                # Scripts for MagicEden integration and NFT minting operations
│   │   │   ├── ABI.js                # ABI definitions for MagicEden integration (to be implemented)
│   │   │   ├── index.js              # Main script for MagicEden NFT minting
│   │   │   └── scripts/
│   │   │       └── apis.js           # API calls for MagicEden integration
│   │   └── Testnet.Free/             # Scripts for free NFT minting on testnet (for demos and testing)
│   │       ├── ABI.js                # ABI definitions for Testnet.Free minting (to be implemented)
│   │       └── index.js              # Main script for Testnet.Free NFT minting
│   ├── BeanSwap/
│   │   ├── ABI.js                    # Exports ABI definitions for Bean-Exchange & token + router contracts
│   │   ├── swap.js                   # Interactive swap script with token approvals, dynamic gas settings, and support for wrapping/unwrapping MON/WMON as well as custom tokens
│   │   ├── liquidity.js              # To be implemented – Script for managing liquidity operations (e.g., adding/removing liquidity)
│   │   └── perps.js                  # To be implemented – Script for handling perpetual contracts trading
│   ├── Kintzu/
│   │   ├── index.js                  # Main script for the Kintzu module (to be implemented)
│   │   └── ABI.js                    # ABI definitions for Kintzu contracts (to be implemented)
│   ├── Synnax/
│   │   ├── index.js                  # Main script for the Synnax module (to be implemented)
│   │   └── ABI.js                    # ABI definitions for Synnax contracts (to be implemented)
│   └── Uniswap/                      # Module for Uniswap protocol operations
│       ├── swap.js                   # Interactive swap script for Uniswap operations
│       ├── ABI.js                    # Exports ABI definitions for Uniswap contracts
│       └── scripts/
│           └── apis.js               # API calls for Uniswap-related operations
├── faucets/
│   ├── official_faucet/
│   │   ├── claim.js                  # Script to claim tokens from the official faucet
│   │   ├── solve_captcha.py          # Python script to solve reCAPTCHA using 2Captcha
│   │   └── scripts/
│   │       └── apis.js               # To be implemented – API calls for the official faucet
│   ├── morkie_faucet/
│   │   ├── claim.js                  # Script to claim tokens from the Morkie faucet; verifies NFT ownership and claims via API
│   │   └── scripts/
│   │       └── apis.js               # API calls for the Morkie faucet
│   ├── owlto_faucet                  # To be implemented – Owlto faucet script
│   └── faucet.trade/
│       ├── add_data.js               # Interactive script to add credentials for the trade faucet
│       ├── captcha.js                # Script to handle captcha challenges for faucet trades using bestcaptchasolver
│       ├── credentials.json          # Credentials for the trade faucet (e.g., API keys, secrets)
│       ├── index.js                  # Main script for the trade faucet module; handles menu for New Wallets, Existing Wallets, Add Credentials, How to add APIs, and Exit
│       └── scripts/
│           └── apis.js               # To be implemented – API calls for the trade faucet
├── index.js                          # Main entry point with interactive menu and child process execution
├── package.json                      # npm dependency configuration and scripts
├── proxies.txt                       # List of proxies (one per line in socks5://login:pass@ip:port format)
├── .gitignore                        # Specifies files/directories to ignore in git
└── .vscode/
    └── launch.json                   # VSCode launch configuration for debugging


## Instructions

1. git clone https://github.com/Tastygeek/MonadTestnet
2. cd MonadTestnet
3. npm install
4. Use some of the following prompts to interact with this CLI

- npm start - (runs index.js main code)
- npm run add - (run node utils/wallet_aggregator.js - allowing you to add your existing addresses)
- npm run generate - (run utils/wallet_generator.js - allowing you to generate new addresses to participate in Monad Testnet)

Good Luck! :)


## Requieriments

1. Set your 2CAPTCHA API on "solve_captcha.py" using "nano faucets/official_faucet/solve_captcha.py" - (currently official faucet no working at all)
2. Set your ACCESS_TOKEN on "captcha.js" using "nano faucets/faucet.trade/captcha.js" from BestCaptchaSolver Website - Here: https://bestcaptchasolver.com/account - Load some funds on your account = Done Example: https://prnt.sc/QgaLKInhRC3t

## Notes

1. Kintzu is added but can't unstake MON if someone knows what's the function corresponding to methodID: "0x30af6b2e" let me know so I can add unstake MON
