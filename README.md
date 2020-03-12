Fabric sdk go sample
==========
`environment:`      
`golang v1.13`  
`fabric v1.4.4`

基于fabric1.4.4 fabric-samples/first-network启动的网络      
通过使用fabric-sdk-go的客户端使用例子

目录:

- config: fabric网络配置
- cli: 链码调用代码封装

## Quick start

1. 启动fabric网络    

```
sh byfn.sh up
```


2. 配置`connection-profile.yaml`

3. 依赖包安装
```
cd fabric-sdk-go-sample
go mod vendor
```

 
4. 进入`samples/chaincode`运行客户端程序`run main.go`

    ```bash
    [root@jc chaincode]# go run main.go
    2020/03/12 18:26:58 Initialized fabric sdk
    2020/03/12 18:26:58 Initialized resource client
    2020/03/12 18:26:58 Initialized channel client
    2020/03/12 18:26:58 =================== Phase 1 begin ===================
    2020/03/12 18:26:58 Install  response status: 200
    2020/03/12 18:26:58 Chaincode has been installed on org1's peers
    2020/03/12 18:27:27 Instantitate chaincode tx: 41a72a79d3ff981ad39cc49df47b38a1c0dbbdd92876a68cbd5cf1cf3e0d4481
    2020/03/12 18:27:27 Chaincode has been instantiated
    2020/03/12 18:27:29 Invoke chaincode response:
    id: 176fa0ad2d7163004c15e8f62be9cd9844efd6c221867fb67b731b595bda9ccb
    validate: VALID
    chaincode status: 200

    2020/03/12 18:27:29 Invoke chaincode success
    2020/03/12 18:27:29 Query chaincode tx response:
    tx: 3342680f5ff915f5e78582975244d0030ab0c239e7bd7307fb745ece594c2e43
    result: 90

    2020/03/12 18:27:29 Query chaincode success on peer0.org1
    2020/03/12 18:27:29 =================== Phase 1 end ===================
    ```