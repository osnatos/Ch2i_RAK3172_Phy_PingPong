# Ch2i_RAK3172_Phy_PingPong

Porting the “SubGHz_Phy_PingPong” project (STM32Cube, NUCLEO-WL55JC) for the  [RAK3172 module](https://docs.rakwireless.com/Product-Categories/WisDuo/RAK3172-Module/Overview).

**Software:**

Project “SubGHz_Phy_PingPong” taken from [STM32CubeWL Firmware Package v1.3.0](https://www.st.com/en/embedded-software/stm32cubewl.html).

**Hardware:**

This project was done using [hallard's RAK3172 breakout board](https://github.com/hallard/RAK3172-Breakout).

**Description:**

This project implements a Ping-Pong application between two Ping-Pong devices.

[RAK3172 breakout boards](https://github.com/hallard/RAK3172-Breakout) were used as such devices.

The applications aims to show a simple RX/TX RF link between the two Ping-Pong devices,

one will be called Ping the other will be called Pong.

By default, each Ping-Pong Device starts as a master and will transmit a "Ping" message, and then wait for an answer.

At start-up, each Ping-Pong Device has its two LEDs blinking.
When boards will synchronize (Tx window of one board aligned with Rx window of the other board)
the Ping Device (board receiving "Ping" msg) will blink green LED and the Pong Device (board receiving "Pong" msg) will blink red LED.
The first Ping-Pong Device receiving a "Ping" message will become a slave and answers the master with a "Pong" message.

Logs via hyper-terminal complement LEDs indicators.

