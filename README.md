# rock5b-multimedia-station-with-mipi

Working on a project that uses the Rock 5B (RK3588) as a multi-purpose media station with MIPI DSI Output and HDMI IN to act as a Smart (4K) Projector

# Status
- This project is currently just a concept/idea, if you are looking for a finished solution, this is not a place for it.
- If you are interested in this project, you may open an issue or comment on my post at Radxa's forum (will update a link after created), feel free to ask any questions. 
- Contributors are HIGHLY ENCOURAGED & WELCOMED for this project, dont be hesitate if you know anything related to any part of this project. Thank you.

# Brief idea and challenge of this Project
Note : This project is a multi-purpose system that combines multiple ideas, it might be complicated to work on.

## IDEA 1 of this project - a DIY 4K Projector

- First, The idea is insired by a YouTube Video [Building a TRUE 4k home cinema projector (it’s awesome)](https://www.youtube.com/watch?v=YfvTjQ9MCwY) by DIY Perks.

### Facts on DIY Perks' IDEA

- NO HDMI INPUT : While it is cool that the video mentioned built a full working 4K Projector, They are using a Sony Phone as the source, which means we have to stick with an Android mobile phone OS, and this means our projector lacks the ability to display content from other sources such as from HDMI.

- NO 4K 60Hz Support : Furthermore, the video mentioned above suggests purchasing the LCD Panel itself via Aliexpress. While you can either purchase this LCD monitor with a MIPI DSI to HDMI adapter, I found that none of the MIPI DSI to HDMI adapter supports HDMI 2.0, which means this solution lacks 4K 60Hz support.

- FORM FACTOR : As you might notice, while without the need of 3D Printing, the video mentioned built its 4K Projector at a really large form factor, and the height of the projector is kinda high. With the help of 3D Printing, I hope we can shrink the form factor of this projector and allows flexibilty to put the projector in both vectically and horizontally.

- BRIGHTNESS & COOLING : As the video mentioned, while you can use a 300W LED Light Source, this brings to the problem of our cooling system and power supply. One of the idea is to use a water cooled radiator (preferrably custom loop) solution, if you have a better idea or solution on this, let us know.

### Advantages of using Rock 5B (RK3588) for this IDEA

- HDMI IN : It is amazing that the RK3588 SoC supports HDMI IN upto 4K 60Hz (HDMI 2.0), that means we can use Rock 5B to accept HDMI sources of our projector

- MIPI DSI @ 4K 60Hz : RK3588 supports upto two MIPI DSI Device upto 4-lane D-PHY v2.0, the Rock 5B comes with a MIPI DSI port which means we can connect an LCD display directly to the device with 4K 60Hz Support

- Multimedia Streaming / Playback : RK3588 supports HEVC, H264, VP9 and AV1 Decoding upto 8K, which means we can easily use Rock 5B to stream services like YouTube, Netflix, Apple TV, etc @ 4K 60 FPS (or above) and allows the projector to use features like AirPlay or Miracast.

### Challenge on IDEA 1

1. Connecting our LCD Display

- Adapter to connect an LCD display to Rock 5B
- Driver for the LCD Display

Since MIPI DSI niether had a standard connector nor a universal display config like HDMI or DP, an adapter is required to connect an LCD Display to the Rock 5B. Additionally, even with an adapter, we will requires a writing / porting of a driver (MIPI DSI Overlay File) to get our LCD display working.

Notes : The Radxa LCD Display works because they have an adapter cable with the display and they have already packed the [overlay file](https://github.com/radxa/kernel/blob/stable-5.10-rock5/arch/arm64/boot/dts/rockchip/rk3588-rock-5b-radxa-10p1inch-display.dtsi) in radxa kernel. Check [this post](https://forum.radxa.com/t/mipi-display-support/12239) for more infomation.



To be written ...
