# Hello-World-Contract
 First app using contracts on the blockchain.
 
To run the code:

1. Install [node](https://nodejs.org/en/).
2. Create Alchemy app with following settings:
    - Chain: `Ethereum`
    - NetWork: `Rinkeby`
    - Environment: `Staging`
3. Change to `Rinkeby Test Network` on [MetaMask](https://metamask.io/).
4. Get Fake Ether from [Chainlink](https://faucets.chain.link/rinkeby).
5. Create file named `.env` in root of project and add the following key-value pairs to it:
    - `API_URL_KEY`=your_api_url_key_from_alchemy
    - `PRIVATE_KEY`=your_wallet_private_key_from_metamask
    - `API_KEY`=your_api_key_from_alchemy
    - `CONTRACT`=your_contract_deployment_address
6. Run the following commands:
    ```
    npm init --yes
    npm install --save-dev hardhat
    npm install dotenv --save
    npm install --save-dev @nomiclabs/hardhat-ethers
    npx hardhat run scripts/deploy.js --network rinkeby
    npx hardhat run scripts/interact.js --network rinkeby
    ```

That's it! you're good to go. You can edit the `.update()` method on `line 23` in file `interact.js` to change the update message to whatever you want and then run the script as well.