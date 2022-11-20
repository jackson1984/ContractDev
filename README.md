# ContractDev
领取测试币

  以太坊浏览器Etherscan发推表示，测试网Rinkeby和Ropsten的浏览器将于2022年10月5日弃用，在可预见的未来，对应将被设置为只读状态，最终将被淘汰。建议开发人员迁移合约并在Goerli或Sepolia上部署新合约。 此前报道，以太坊Kiln测试网将于本周关闭，Ropsten和Rinkeby测试网也将于2022年第四季度和2023年第二季度分别关闭。
  
  1、注册Alchemy
  https://alchemy.com/?r=4ede9c8014f71838
  
  2、登录Alchemy，创建测试APP
  在Truffle-config.js中，配置Network时使用创建的测试APP的API KEY。点击VIEW KEY，弹窗框中HTTPS
  ```javascript
    goerli: {
      provider: () => new HDWalletProvider(mnemonic, `https://eth-goerli.g.alchemy.com/v2/XXXXXXXXXXXX`),
      network_id: 5,       // Ropsten's id
      //gas: 30000000,        // Ropsten has a lower block limit than mainnet
      //gasPrice: 30000000000,
      // confirmations: 2,    // # of confs to wait between deployments. (default: 0)
      // timeoutBlocks: 200,  // # of blocks before a deployment times out  (minimum/default: 50)
      // kipDryRun: true     // Skip dry run before migrations? (default: false for public nets )
    },
  ```
  3、登录水龙头，粘贴钱包地址
  https://goerlifaucet.com/
