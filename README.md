AVR V-USB custom skelton project
================================


Faça um dispositivo USB personalizado com AVR + V - USB Skeleton V - USB responde pedidos padrão e pode ser escrito de forma bastante concisa.

Exemplo de implementação do host para conexão a este dispositivo

./sketch.rb libusb + ruby
./sketch-chrome-app/ Chrome App
Exemplo de circuito (Eagle)

./circuit/
 Antecedentes

Mac: Uma vez que o sistema operacional possui acesso de baixo nível ao dispositivo HID, criar um dispositivo como uma classe HID é bastante incômodo (embora o controle_transfer seja possível, mas claim_interface é impossível, você não pode fazer mais nada) ).

 Memorando

USB_CFG_DEVICE_CLASS para 0xff (fornecedor)
USB_CFG_INTERFACE_CLASS para 0xff (fornecedor)
Se você não fizer isso (claim_interface falha)

ref.

http://vusb.wikidot.com/driver-api
http://vusb.wikidot.com/host-software

AVR V-USB custom class skelton project
======================================

AVR + V-USB でカスタムUSBデバイスを作るスケルトン
V-USB がスタンダードなリクエストには答えてくれるのでかなり簡潔に書ける。

このデバイスに接続するためのホスト実装のサンプル

 * [./sketch.rb]( ./sketch.rb ) libusb + ruby
 * [./sketch-chrome-app/]( ./sketch-chrome-app/ ) Chrome App

回路図の例 (Eagle)

 * [./circuit/]( ./circuit/ )

## 背景

Mac の場合 HID デバイスへの低レベルアクセスを OS が握っているため、
HID クラスとしてデバイスを作成すると、かえって面倒なことになる ( control_transfer は可能だが、claim_interface が不可能なので他のことは何もできない)。


## 覚書

 * USB_CFG_DEVICE_CLASS を 0xff (vendor)
 * USB_CFG_INTERFACE_CLASS を 0xff (vendor)

にしないとダメ (claim_interface が失敗)


ref.

 * http://vusb.wikidot.com/driver-api
 * http://vusb.wikidot.com/host-software
