
# Theta Metamask Demo : Andrew Lunde Version

A Theta-Metamask demo based on @jacobedawson's [tutorial](https://github.com/jacobedawson/connect-metamask-react-dapp), which showcases a working React app that will be able to connect to your MetaMask account, and read your address and TFuel balance. If you connect with multiple accounts the interface will change to reflect the active account.

## Setup

First, connect your **Metamask plugin to the Theta Mainnet** following the instructios [here](https://docs.thetatoken.org/docs/web3-stack-metamask#connect-metamask-to-the-theta-mainnet).

Next, clone this repo and install dependencies:

```
git clone https://github.com/andrewlunde/theta-metamask-demo
cd theta-metamask-demo
npm install
```

As an extra step, we need to build and copy over the Theta fork of the `useDApp` lib. This step can be skipped after this [pull request](https://github.com/EthWorks/useDApp/pull/326) gets merged.

```
cd ..
git clone https://github.com/thetatoken/useDApp
cd useDApp
yarn
yarn build
cd ../theta-metamask-demo
rm -rf node_modules/@usedapp/core
cp -r ../useDApp/packages/core node_modules/@usedapp/
```

## Run React dev server
 
Execute the following command to launch the web client at http://localhost:3000

```
npm start
```

## Run React production server

### 6079SmithW [George Orwell 1984 Telescreen Exercise](https://youtu.be/CCfW6HFP5cI?t=26)
### [React Deployment](https://create-react-app.dev/docs/deployment/)

```
npm run-script build
serve -s build -l 6079

- Local:             http://localhost:6079
- On Your Network:   http://192.168.1.84:6079
- External Internet: http://70.251.209.207:6079
```

You should see the web page displays the TFuel balance in your Metamask plugin and the wallet address.

## Other Resources
```
https://web3js.readthedocs.io/en/v1.5.2/index.html
https://cryptozombies.io/en/lesson/6/chapter/1
```