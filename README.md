# Croissant Breadboard Prototyping Tool
The Croissant is a multi-function PCB that lets you use your existing synthesizer equipment with a standard breadboard, with plenty of addons and extras.
Check out the video! [https://youtu.be/_RGXiyb1UPI?si=hu-ymMrpfnG7xpGm] (https://youtu.be/_RGXiyb1UPI?si=hu-ymMrpfnG7xpGm)

![Croissant Render](https://github.com/user-attachments/assets/55de5797-36c9-4250-9751-c105d5e203f0)

One day, I was using a breadboard to test out a circuit design for my synthesizer, and I was trying to hold a headphone jack and a power connector with its cable onto the board with one hand, and another headphone jack with another hand, all while trying to turn a knob on the synth. That made me think there had to be a better way to get synthesizer components onto a breadboard, so I make just such a tool. It's shaped like a C and it goes on a breadboard, so I called it the Croissant.

The primary feature is a combined footprint for Pocket Rack (Molex SL) and Eurorack (5x2 pin shrouds) power connectors that routes +12v, Ground, and -12v to the power rails of a breadboard via pin headers. This lets you use your existing equipment on a breadboard and power it with the actual synth you will eventually use your designs in.

## Configurations
### Minimal
To use the Croissant in its most basic mode, all you need to do is add a power connector of your choice, jump the two pads labeled "0 Ohm Bypass", and install a power switch or jump the pins.
![Croissant Minimal Config](https://github.com/user-attachments/assets/de8594f3-1ab8-4264-80d9-7672878e656b)

### Reverse Polarity
Alternatively, you can add the capacitors and diodes for reverse polarity protection and NOT jump the 0 Ohm Bypass to guarantee your +12v and -12v lines are always just that.
![Croissant Reverse Polarity](https://github.com/user-attachments/assets/5fad47d6-a9d6-447a-bcac-d66ab94663ee)

### Peripherals
In addition, the Croissant has two slots that can each fit either a vertical 3.5mm stereo jack, a horizontal jack, or a potentiometer. These connections are routed to the breadboard as well, both on the inside where the power is attached, but also on the edge of the Croissant so you can use more than one of them at a time on your breadboard.
![Peripherals](https://github.com/user-attachments/assets/3ef5871e-c94c-44e6-9dd5-6390362ccac7)

### 3.3v and 5v Lines
There are also two footprints for adding two linear regulators (through-hole or surface-mount in the same footprint) and their associated capacitors. The board is labeled for 3.3v and 5v for microcontrollers such as a Raspberry Pi Pico or an Arduino.
![Croissant 3_3v](https://github.com/user-attachments/assets/88aa8ab2-dc3f-474a-aaf5-4c3247c643b0)
![Croissant 5v](https://github.com/user-attachments/assets/578557a3-7271-4233-802a-54a490d152de)

### Amp
Also, since the price at most PCB fabs is the same either way, I added a small audio amplifier board to the middle of the Croissant that you can snap out. I designed it around an FM8002A based on this video: https://www.youtube.com/watch?v=I4WP1u4hwpw
I haven't tried this out myself yet, so I can't confirm if it works. I hope to soon once the parts come in. The datasheet recommended tying the positive input pin to ground and connecting the audio in to the negative input, but that sounded odd to me even if this is exclusively supposed to be an inverting amplifier. I made a footprint pattern with 0 Ohm resistors in a square where if they are soldered as the silkscreen indicates, they will produce this configuration. If these resistors are both rotate 90 degrees, that will route the audio in to the positive input of the FM8002A and tie the negative input to ground.
![Amp](https://github.com/user-attachments/assets/2925b0fe-9095-47c7-845b-a7edb04adf61)

I only started learning PCB design a few months ago, so I'm always open to suggestions and improvements!
