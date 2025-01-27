# Respi-car
- 测试环境：Windows 11

- 运行环境：树莓派5（8GB RAM） arm64 aarch64 PIOS 64位
  - 运行环境下引入pygame库需要 conda install -c conda-forge gcc 否则会报错。

- 用gpiozero库操作GPIO默认工厂为PRI.gpio，其输出的PWM抖动非常大，舵机无法正常使用。需要更换为pigpio引脚工厂。该引脚工厂需要先安装sudo apt install pigpio，然后启动服务sudo systemctl enable pigpiod（开机自启动）sudo systemctl start pigpiod（启动服务）
- pygame.camera需要安装opencv才能使用