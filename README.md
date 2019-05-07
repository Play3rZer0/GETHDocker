# GETHDocker
Running GETH (Ethereum Go) node from a Docker Container.

The GoEthereum website lists the following available images with descriptions.
ethereum/client-go:latest is the latest develop version of Geth
ethereum/client-go:stable is the latest stable version of Geth
ethereum/client-go:{version} is the stable version of Geth at a specific version number
ethereum/client-go:release-{version} is the latest stable version of Geth at a specific version family

The following ports are opened by default when running from the container.
8545 TCP, used by the HTTP based JSON RPC API
8546 TCP, used by the WebSocket based JSON RPC API
30303 TCP and UDP, used by the P2P protocol running the network
30304 UDP, used by the P2P protocol's new peer discovery overlay

For more details, read the article at this link at FreeCodeCamp.org:

https://medium.freecodecamp.org/how-to-run-geth-from-a-docker-container-b6d30620ca74

Take note that running the option rpcaddr “0.0.0.0” is not secure, since you are opening up your node to all traffic. If your ETH wallet were unlocked, a hacker can get to your node in this way and take your coins. I don’t cover security in this article, but you can read more about that here -> https://medium.com/coinmonks/securing-your-ethereum-nodes-from-hackers-8b7d5bac8986 (securing your GETH node’s RPC ports). Always abide by safe and best practices.
