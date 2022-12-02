# Dusk cüzdan güncellemesi (yeni sürüm)

```
wget https://github.com/dusk-network/wallet-cli/releases/download/v0.13.0/ruskwallet0.13.0-linux-x64-libssl3.tar.gz
```
```
tar -xf ruskwallet0.13.0-linux-x64-libssl3.tar.gz
```
```
cd rusk-wallet0.13.0-linux-x64-libssl3
```
```
ln -s ./rusk-wallet /usr/local/bin
```




# Dusk-stake


## stake işlemimizi yapıyoruz bu kodla cüzdanımızı kendi nodemuz üzerinden çalıştırıyoruz doğal olarak stake ve ödül çekme işlemlerini yapabiliyoruz. isteyen yapanilir
```
cd rusk-wallet0.13.0-linux-x64-libssl3/
```
```
./rusk-wallet --state http://127.0.0.1:8585
```
* Girdikten sonra `Stake Dusk` diyoruz
* Miktar: `29995` (30k geldi, biraz fee için vs. bırakın)
* Gas limit: `2500000000`
* Gas price: Burada direkt tab tuşuna basın, var sayılan dışına çıkamazsınız
* Sonra Y diyip enterliyoruz
* 30/30 işlem gerçekleşecek ve bit TX HASH verecek bize
* Eğer burada SUCCES yazıyorsa aratınca, işlem tamam: [Explorer Linki](https://explorer.dusk.network/transactions/)

## Node kontrol:
```
tail -100 /var/log/dusk.log | grep 'Accepted'
