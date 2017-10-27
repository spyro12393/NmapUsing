# Nmap - Network Mapper
- Questions
    - 說明nmap指令中各項option參數的意義
    - 設計不同情境以展現nmap的功用


## 1. 什麼是通訊埠？What is a **Port**?
### Protocal Port
- 是一種經由軟體建立的服務，在一個電腦作業系統中扮演通訊的端點（endpoint）。每個通訊埠都會與主機的IP位址及通訊協定關聯。
Example:`172.20.80.24:9100`

- 通訊埠以16位元數字來表示，這被稱為通訊埠編號（port number）。
![](https://i.imgur.com/2Esoqdw.png)


## 2. What is Nmap?
- Network Mapper
- Nmap（網路對映器）是一款用於網路安全的工具，他屬於自由軟體，因而可以免費下載。
- Nmap 長得像：
![](https://i.imgur.com/HtJqKLo.png)

```graphviz
digraph hierarchy {

                nodesep=1.0 // increases the separation between nodes
                
                node [color=Red,fontname=Courier,shape=box] //All nodes will this shape and colour
                edge [color=Blue, style=dashed] //All the lines look like this

                Nmap->{列舉網路主機清單 監控主機 服務執行狀況}
}
```
- `狀態`可能是 open(開放的)，filtered(被過濾的)， closed(關閉的)，或者unfiltered(未被過濾的)

- `Open(開放的)`意味著目標機器上的應用程序正在該端口監聽連接。
- `filtered(被過濾的)` 意味著防火牆，過濾器或者其他的網路障礙阻止了該端口的訪問，Nmap無法得知他是open還是closed。 
- `closed(關閉的)` 端口沒有應用程序在他上面監聽，但是他們隨時可能開放。
- `unfiltered(未被過濾的）當端口對Nmap的探測做出響應，但是Nmap無法確定他們是關閉還是開放時，這些端口就被認為是unfiltered(未被過濾的），如果Nmap報告狀態組合 open|filtered 和 closed|filtered時，那說明Nmap無法確定該端口處於兩個狀態中的哪個狀態。


## 3. What are the "options"?



## 4. Implementation.


----
# The End

