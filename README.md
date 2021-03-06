# robosys_device_driver

Device driver that can handle LED on Raspberry Pi.

## 概要
入力する値によってLEDの点滅のパターンが変わるデバイスドライバです。点滅のパターンは、モールス信号を表します。

## 動画
* URL - https://www.youtube.com/watch?v=E9WvXxnSEjY

## 使うもの
* Raspberry Pi 3 Model B
  * Raspbian
* LED
  * GPIO25, GNDに接続

## 使い方
1. リポジトリを clone し、build
```
$ git clone https://github.com/takumo3o/robosys_device_driver.git
$ cd robosys_device_driver
$ bash maker.bash
```

2. 0~2 の内の好きな数字を入力
```
$ echo 0 > /dev/myled0
$ echo 1 > /dev/myled0
$ echo 2 > /dev/myled0
```
  * 0の場合: チクワ
  * 1の場合: ダイコン
  * 2の場合: ギュウスジ
    * それぞれをモールス信号で表している。

3. clean
```
$ bash cleaner.bash
```
  * build 後の led.c への変更の反映や、環境をきれいにしたい際に clean

## LICENSE
このリポジトリは GPLv3 ライセンスに基づきます。[LICENSE](https://github.com/takumo3o/robosys_device_driver/blob/master/LICENSE)をご覧ください。
