# ZYBO_Z7-20_u-boot_uImage
Digilent社のZYBO Z7-20のビルド済みのBOOT.bin とdevicetree(devicetree.dtb)です。デバイスツリーのソースコードがzynq_zybo_z7.dtsです。
入っているビットファイルは、ガボール・フィルタ入りの白線走行用畳み込みニューラルネットワークです。いずれもカメラが無いと使用でき無いのが残念です。
http://marsee101.blog19.fc2.com/blog-entry-3943.html

BOOT_Z7_gpio.bin と devicetree_Z7_gpio.dtb の組がAXI GPIO が入ったビットファイルです。デバイスツリーのソースコードがzynq_zybo_z7_gpio.dtsです。
http://marsee101.blog19.fc2.com/blog-entry-3934.html
http://marsee101.blog19.fc2.com/blog-entry-3935.html

uImageがLinuxカーネル(GNU/Linux 3.14.0-xilinx-13567-g906a2c9-dirty armv7l)です。古いですが、最初のテストには良いと思います。対応するu-boot がu-boot_zed.elfです。Zedboard 用のu-bootですが、ZYBO Z7-20で問題なく立ち上がります。
nEnv.txtも必要なので、Linuxカーネルと一緒のSDカードのフォルダに入れておいてください。

RootFSも入れておきたかったのですが、大きくて入りません。私は、Vivado and zybo linux勉強会資料3のUbuntu 14.04のRootFSを使用しています。
https://www.slideshare.net/marsee101/vivado-and-zybo-linux3

後のRootFSは、「BRAVO FPGA」さんの「ZYBO27 (Linux + simple framebuffer でX Windowを動かすまで 2)」
http://bravo-fpga.blogspot.jp/2016/12/zybo27-linux-simple-frame-buffer-x.html

linaro-jessie-alip-20160913-31.tar.gz
https://releases.linaro.org/debian/images/alip-armhf/latest/
でも良いかもしれません。

また、PYNQボードのイメージもBOOT.bin とデバイスツリー、uImageを入れ替えることで動作しました。（ただしVer.1で試しています）
http://pynq.readthedocs.io/en/latest/getting_started.html

ただし、ZYBO Z7-20はPYNQとハードウェアが違うので、ビットファイルをコンフィギュレーションしても動作しません。また、壊れるかもしれません？壊れても保証できないので絶対にやらないでください。

注）BOOT_Z7_gpio.bin と devicetree_Z7_gpio.dtb を使う場合には、BOOT.bin と devicetree.dtb にリネームしてください。


ライセンスはGPL v2とします。
