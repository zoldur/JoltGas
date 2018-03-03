# Jolt Gas
Shell script to install a [Jolt Gas Masternode](https://www.ijolt.us/) on a Linux server running Ubuntu 16.04. Use it on your own risk.

***
## Installation:
```
wget -q https://raw.githubusercontent.com/zoldur/JoltGas/master/jolt_install.sh  
bash jolt_install.sh  
```
***

## Desktop wallet setup

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps for Windows Wallet
1. Open the Jolt Gas Desktop Wallet.
2. Go to RECEIVE and create a New Address: **MN1**
3. Send **2000** **JLG** to **MN1**.
4. Wait for 15 confirmations.
5. Go to **Tools -> "Debug console - Console"**
6. Type the following command: **masternode outputs**
7. Go to  ** Masternodes -> Create"
8. Add the following entry:
```
Alias Address Privkey TxHash Output_index
```
* Alias: **MN1**
* Address: **VPS_IP:PORT**
* Privkey: **Masternode Private Key**
* TxHash: **First value from Step 6**
* Output index:  **Second value from Step 6**
9. Click OK and exit the Wallet.
10. Open Jolt Gas Wallet, go to **Masternode Tab**. If you tab is not shown, please enable it from: **Settings - Options - Wallet - Show Masternodes Tab**
11. Click **Update status** to see your node. If it is not shown, close the wallet and start it again.
10. Click **Start All**
11. If you are not able to see your **Masternode**, try to close and open your desktop wallet.
***

## Usage:

```
joltgasd getinfo
joltgasd masternode status
```

Also, if you want to check/start/stop **Jolt Gas** , run one of the following commands as **root**:

```
systemctl status JoltGas #To check the service is running.
systemctl start JoltGas #To start JoltGas service.
systemctl stop JoltGas #To stop JoltGas service.
systemctl is-enabled JoltGas #To check whetether JoltGas service is enabled on boot or not.
```
***


## Donations:  

Any donation is highly appreciated.  


**BTC**: 1BzeQ12m4zYaQKqysGNVbQv1taN7qgS8gY  
**ETH**: 0x39d10fe57611c564abc255ffd7e984dc97e9bd6d  
**LTC**: LXrWbfeejNQRmRvtzB6Te8yns93Tu3evGf
