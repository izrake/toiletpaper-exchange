# Toiletpaper.Exchange

## Goal of this project
Education around arweave, profit sharing communities, currencies & decentralization.


## Smart Contracts
1. FedSmartContract: representing the Fed - issuing 1 US Dollar Wipepaper (UWP) per week  
2. EZBSmartContract: representing the EZB - releasing 1 Euro Wipepaper (EWP) per week  
3. The Betting Smart Contract

## PSTs
1. US Dollar Wipepaper (UWP)  
2. Euro Wipepaper (EWP)


## Frontend
Under construction --> we use [vue](https://cli.vuejs.org/) to develop our client code.  

If you are completely new to nodejs and vue you might try the following steps on your machine.  

1. install [NodeJS](https://nodejs.org/en/)
2. install vue via the following command ```npm install -g @vue/cli```
3. vue create client 
4. cd client
5. npm run serve
6. visit http://localhost:8080/

Tipps: 
I use [VS Code Insiders](https://code.visualstudio.com/insiders/) as my IDE.  
Installing [these extensions](https://github.com/michael-spengler/toiletpaper.exchange/blob/main/.vscode/extensions.json) might also be valuable for you.  
You might want to simplify your life by using vuetify: https://www.youtube.com/watch?v=CjXgoYo86yY
```
vue add vuetify
```
## Backend
We'll use Smart Contracts deployed on the Ethereum Blockchain + Deno & Web3 (we need to check [this open issue](https://github.com/ethereum/web3.js/issues/3700)).  

**Links which might be helpful**
1. https://github.com/useverto/trading-post/blob/master/src/workflows/swap.ts  
2. https://docs.chain.link/docs/ethereum-addresses    
3. Video on a chainlink based Dapp: https://www.youtube.com/watch?v=YLmMNocc1ys  
4. Off-Chain data provisioning and inter-blockchain interoperability: https://www.youtube.com/watch?v=-pUR9WPIrX0


## Deployment Options
We need to provide the page and the data to users. Here are some options for those topics.
### Providing the Page
**Option 1: Using GitHub Pages**

**IP Addresses:**  
185.199.108.153  
185.199.109.153  
185.199.110.153  
185.199.111.153  

https://docs.github.com/en/free-pro-team@latest/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site

**vue.config.js**
```
module.exports = {
    publicPath: "./",
    outputDir: "./docs"
  };
```

--> run npm run serve after this file update and visit: http://localhost:8080   

details see https://blog.usmanity.com/serving-vue-js-apps-on-github-pages/


**Option 2: Using Deno with Opine**
This option would require for a central server on which you could execute the content of [deno-opine-page-server.ts]() via:  
```
deno run --allow-read --allow-net deno-opine-page-server.ts
```

### Providing Data 
We will connect our page with the Ethereum blockchain. Details follow.


## Feedback & Contact
In case of any feedback, please raise an issue [here](https://github.com/michael-spengler/toiletpaper.exchange/issues/new).