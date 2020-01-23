### BlockChain Instructions

1. Open a terminal window and navigate to your `Blockchain-Tools` folder and imput the following 
  ./puppeth

2. Specify a name for the network

3. Type 2 to "Configure new genesis" 

4. Type 1 to "Create new genesis from scratch"

5. Type 1 to choose "Proof of Authority"

6. Paste in cloud mneumonic in MyCrypto and choose 2 addresses.

7. Paste in addresses on command line excluding "0x" and hit enter, hit enter again on the blank line to continue

8. When prompted to prefund accounts with wei, paste in both address again

9. Choose a "chain ID" ex: 340, then hit enter

10. Type 2 to "Manage existing genesis"

11. Type 2 to 'Export genesis configurations" 

12. .Json files will be create in the Blockchain-Tools folder

13. Ctrl+C to exit the puppeth prompt



### 8. Create Nodes
14. Type following code to command line
./geth account new --datadir node1

15. Input a password for node 1

16. Repeat for node2

17. Initialize nodes by typing the following on the command line

./geth init puppernet.json --datadir node1
./geth init puppernet.json --datadir node2


### 12. Starting the Blockchain 

18. Mine the first node with the following command:
./geth --datadir node1 --mine --minerthreads 1

19. Find the "enode://" address and copy (save for later)

20. Open another terminal window and navigate to your Blockchain Tools folder

21. launch second node with the following command:

  ./geth --datadir node2 --port 30304 --rpc --bootnodes "enode://69994ca26f775569b5cdb4970299c2265f7dcb7714a4ffaf66400f50e5128e79e2ff465731ddf597030f931375aa90f40d6cff7ace0f4afb84ae8de19da047bf@127.0.0.1:30303"

### Transacting on the chain 

### Getting address key
22. Open MyCrypto and choose the "Kovan" network

23. Unlock your wallet using your mnemonic phrase

24. Choose the ETH address you use to pre-fund your chain, select "Wallet Info.

25. Click on the eye icon next to the "Private Key" and copy the private key of the wallet.

26. On the left of MyCrypto, click "Change Network"

### seting network info
26. Click on "Add Custom Node", then add the custom network name chosen earlier.

27. Scroll down to choose "Custom" in the Network settings

28. Update chain ID and must match the chain ID on command line

29. Add URL: `http://127.0.0.1:8545`

30. Click on "Save & Use Custom Node"

#### Sending money

31. On the left menu, click on "View & Send"

32. Click on the "Private Key" option

33. Paste the private key of the pre-funded wallet and click "Unlock"

34. Paste the second address into the "To Address" field, choose an ammount of ETH to send.

35. Confirm transaction by clicking "Send Transaction"

36. Click "Check TX Status" to check the status of your transaction
