-include ../.env

.PHONY: build deploy-sepolia clean

build:; forge build

deploy-sepolia:
	forge script script/DeployFundMe.s.sol:DeployFundMe --rpc-url $(SEPOLIA_RPC_URL) --network-id $SEPOLIA_NETWORK_ID --from $SEPOLIA_FROM --private-key $(SEPOLIA_PRIVATE_KEY) --private-key $(PRIVATE_KEY) --broadcast --verify --etherscan-api-key $(ETHERSCAN_API_KEY) -vvvv

clean:; forge clean