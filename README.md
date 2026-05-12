# Pulse Width Modulation on General Purpose Timer

### What this project is
This project is created to examine what is a Pulse Width Modulation, how it works, where it
can be used, its architecture and logic. This project is developed according to online course [Mastering Microcontroller: Timers, PWM, CAN, Low Power(MCU2)](https://www.udemy.com/course/microcontroller-programming-stm32-timers-pwm-can-bus-protocol/learn)
by Kiran Nayak (FastBit Embedded Brain Academy).

### What the PWM is
Pulse Width Modulation is the way to reach analog effect (smooth handling) by
digital tools, changing a voltage application time. The main idea is to configure a period of high (1)
and low (0) states on a line. The longer period of logic 1, the bigger "efficient power". The PWM is 
uses for configuring LED brightness, motor speed, handling servos, sound, etc. Also, it allows to decrease 
CPU load.

### What actually this program does
- enables TIM2
- configures TIM2 as general purpose timer
- configures all 4 TIM2's (CH1-CH4) channels into PWM mode
- configures duty cycles for all channels as 25% for CH1, 45% for CH2, 75% - CH3, and 95% - CH4

### How to measure duty cycles
In this case I used my 8-channel Saleae Logic Analyzer clone and measured every channel (PA0 is CH1, PA1 - CH2, PA2 - CH3, PA3 - CH4).
Here is the results:

![PulseView screen](image/Pasted%20image.png)

### Used devices
- MCU: **STM32F407VET6**
- CPU: **ARM Cortex-M4**
- Debugger: **WeAct 1.0**
- Logic Analyzer: **Sealae 8-channel clone**

### Used software and documentation
- Programming language: **C**
- Implementation: **HAL**
- IDE: **CLion**
- STM32 Project editor: **STM32CubeMX**
- Reference Manual: **RM0090**
- Logic Analyzer Tool: **PulseView**