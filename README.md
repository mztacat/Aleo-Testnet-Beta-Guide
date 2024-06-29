# Aleo-Testnet-Beta-Guide
Prior testnets have shown that while consumer-grade hardware can technically participate as a prover, it is unlikely to be effective due to high level of competition.







------------------
# Requirement  
## Aleo Prover that is competitive, the machine will need more than these requirements.
![image](https://github.com/mztacat/Aleo-Testnet-Beta-Guide/assets/31314340/bb2a8efd-77d5-48ed-ab63-9f55e5f793ec)







## Updating System 
```
sudo apt update && sudo apt update -y
```
![image](https://github.com/mztacat/Aleo-Testnet-Beta-Guide/assets/31314340/99855651-9207-404c-86e9-4db3b24f4dd8)


### Install GIT
Reply with ```y``` and continue 
```
sudo apt install git
```

## Install Rust 
Reply with ```y``` and continue 
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

```

### Set Environment PATH
```
. "$HOME/.cargo/env"
source ~/.bashrc   
```

### Update RUST & Check version 
```
rustup update
rustc --version
```
![image](https://github.com/mztacat/Aleo-Testnet-Beta-Guide/assets/31314340/02daf804-3493-45b8-a72b-2d1d380cc47a)




## Clone SnarkOS Repository 
```
git clone --branch mainnet --single-branch https://github.com/AleoNet/snarkOS.git
cd snarkOS
git checkout tags/testnet-beta
```

![image](https://github.com/mztacat/Aleo-Testnet-Beta-Guide/assets/31314340/9bd099a1-d490-4d60-be9b-fd38d68144ee)



## Install dependencies 
```
./build_ubuntu.sh
```
![image](https://github.com/mztacat/Aleo-Testnet-Beta-Guide/assets/31314340/356c1d44-0d3a-4ed8-a9c8-1de1f1e7960a)  
![image](https://github.com/mztacat/Aleo-Testnet-Beta-Guide/assets/31314340/d8f90d89-8427-49f8-a80f-906f1544f068)

![image](https://github.com/mztacat/Aleo-Testnet-Beta-Guide/assets/31314340/9bb40d61-ac91-4ad5-a524-c1a56498fba0)


## Install SnarkOS 
```
cargo install --locked --path .
```
![image](https://github.com/mztacat/Aleo-Testnet-Beta-Guide/assets/31314340/cd20516e-f2e5-4e98-a594-57460346346b)




## Open required port 

```
sudo ufw allow 4130/tcp
sudo ufw allow 3030/tcp
sudo ufw allow ssh
sudo ufw enable
sudo ufw status
```
![image](https://github.com/mztacat/Aleo-Testnet-Beta-Guide/assets/31314340/e56401ec-12a7-4c5c-a42c-9ae9dca34075)



## Run ALEO Node
### Run CLient before PROVER! 

### Open Screen 
```
screen -S client
```
![image](https://github.com/mztacat/Aleo-Testnet-Beta-Guide/assets/31314340/435c5534-f30a-45c7-88c5-b32ef3ffce45)



```
./run-client.sh
```
![image](https://github.com/mztacat/Aleo-Testnet-Beta-Guide/assets/31314340/d3b82fb0-0139-412c-a95a-b6e5707ca5ac)








### COMPILING























