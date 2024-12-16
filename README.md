# reddcoin
reddcoin update if you in wrong chain
run /statistics in ReddCoin telegram  
![image](https://github.com/user-attachments/assets/b6da4e8a-3172-4d2b-9837-1de5ed975bf8)  
Go to Window->Information to compare Block height 
![image](https://github.com/user-attachments/assets/ad34abe0-d6a2-4cd1-a761-ae79b87bf69d)  

If there is different in Current Block Height Information then follow Obito Instruction  
![image](https://github.com/user-attachments/assets/4950f003-4432-4d54-8957-5567adbce486)  


## Obito Instruction
![image](https://github.com/user-attachments/assets/5c15b6a1-500d-489d-a262-1217eedf05d4)  
It's because your ReddCoin Core Wallet is on the wrong chain. You will not be able to send and receive coins unless you'll get back to the right chain.

We had two bad blockchain splits. First at block 5448005 and the second one at block 5519068.
1. To verify if you're on the first bad fork run in the Console of the Core Wallet:
   ```sh
   getblockhash 5448005
   ```
   If the output of this command is  
   `99e1ba495f4da89c2a0c8a0296cb1df69d5a76488c06517a5aee5c0000c496da`
   then you're on the right chain.  
   If the output is  
   `809a59a737c3479ac17ad0fd426193596cc02cfb82cd1c87fa05ef94f8f8587a`  
   then you're on the wrong chain.
   ![image](https://github.com/user-attachments/assets/df0f2e3e-0d2d-41f9-aec9-6ea9a5cca779)  
2. To switch from the first fork to the correct chain you must run the command:  
   ```sh
   invalidateblock 809a59a737c3479ac17ad0fd426193596cc02cfb82cd1c87fa05ef94f8f8587a
   ```
   Wait for several minutes for Executing...
4. To verify if you're on the second bad fork run in the Console of the Core Wallet:
   ```sh
   getblockhash 5519068
   ```
   If the output of this command is  
   `1d6ebb2d73dccc03b7b9b013c3b08ec8a83919ed4480edbad6e0604be53f5b40`
   then you're on the right chain.  
   If the output is  
   `420d82c48eea24cd9a06b24cc012bb89abdcab95bdbc29ef02d9fd55ef41f570`  
   then you're on the wrong chain.
6. To switch from the second fork to the correct chain you must run the command:
   ```sh
   invalidateblock 420d82c48eea24cd9a06b24cc012bb89abdcab95bdbc29ef02d9fd55ef41f570
   ```
   After that compare in real-time the block height from your Core Wallet with the block height from the blockchain explorer.
8. To see the block height from your wallet, run the command getblockchaininfo or hover the cursor over the icon from the bottom right of the wallet. The block heights must be the same.
If you are on the first bad fork, after you switch to the right chain, let the wallet sync with the network and check (run the command) to see if you're not in the second bad fork. At the end, the block height from your wallet should be the same with the block height from the blockchain explorer.
https://blockbook.reddcoin.com

After you'll get back to the right chain you will see the coins back to the balance and you will lose all the stake rewards that you received while you were on the wrong chain (you will see the transactions greyed-out and the stakes substracted from your balance).

PS. Do not reply to anyone who writes to you privately because I have noticed that scammers tend to do this when someone asks for help.
