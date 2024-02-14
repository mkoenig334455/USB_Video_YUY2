USB_Video_STM32F407VGTX_YUY2 example USB and VIDEO class

This example will create a "camera interface" in the windows "device manager" by USB. 
You can open the camera device by VLC or windows camera and you will se two pictures toggeling as video stream (pink and green)

I use: STM32CubeIDE 1.14.0 CubeMX 6.10.0 STM32F407VGTX + PHY USB3310 / USB HighSpeed


There is a problem. when you enable USB/DMA in the usb_otg.c file:
 hpcd_USB_OTG_HS.Init.dma_enable = ENABLE;
In that case the video stream works only one time at the first camera app start. When you close the camera app an start the app again the dma will not work!
I didn't find the reason so far....
