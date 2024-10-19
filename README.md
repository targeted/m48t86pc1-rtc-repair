# M48T86PC1 RTC chip battery repair

How to repair an M48T86PC1 RTC chip by attaching an external CR2032 coin battery to it.

STM [M48T86PC1](https://www.alldatasheet.com/datasheet-pdf/pdf/22989/STMICROELECTRONICS/M48T86PC1.html) is a real-time clock package,
found in retro PC motherboards. It is similar in function to well-known DALLAS 12887 et al. As such, it contains a lithium battery,
which loses power after some 10 years and the motherboard stops working properly.

One way of repairing RTC chips is to drill the case and connect an external coin battery instead of the empty internal one.

I attempted to repair one M48T86PC1 by following the instructions for DALLAS 12887 (many around, see [this](https://www.youtube.com/watch?v=NdlSfqto_0o) for example)
but it turned out that the battery location inside is different, and before I knew it, I drilled the entire casing away and destroyed the chip in the process.
But the second time I knew where to drill and solder and here I share the step-by-step instructions. 

## Disclaimer

If you decide to follow this manual, you do it on your own risk. I'm not responsible for any damages or consequences.

## Theory

The internal lithium battery inside M48T86PC1 is located to one side of the case, with connecting pins stretching outwards to the side, like so:

![image](https://github.com/user-attachments/assets/fde7a280-3d97-4972-bd98-731e190005db)

Therefore there is a difference in where the holes must be drilled compared to DALLAS:

![image](https://github.com/user-attachments/assets/e1832cea-2ec1-4295-aaea-9a4095b2911d)

and here is the close up diagram of where to drill:

![image](https://github.com/user-attachments/assets/c5843b6b-4252-4f7c-8e15-0ebcb38aceb3)

Note that you need to drill two holes, one against the ground (-) connector pin on the left, and one against the positive (+) battery connector pin on the right.

## Practice

The initial battery view:

![image](https://github.com/user-attachments/assets/ca183b3c-662d-45a5-9547-770762951dda)

![image](https://github.com/user-attachments/assets/87acc553-e97d-439c-905b-aa2dbb775d6a)

You may need a Dremel-like tool with a plastic drilling flat bit. 

Drill two small round holes at those positions, 
about 1-2 mm deep, until you hit metal. Measure the voltage between the two points that you have. My device was 
actually new, therefore it measured 3.3 volts, but for a "dead" one, it could be under 0.5 volts.

![image](https://github.com/user-attachments/assets/9ee2d061-fd6b-468a-9ed9-cc911eab26a2)

Keep drilling around to make two vertical cylindrical shafts around the exposed connectors:

![image](https://github.com/user-attachments/assets/687a4bb5-bf8e-44d3-986c-6f1eca3006b0)

The positive connector should be broken between the solder point and the internal battery,
so that it is not being charged by the externally installed battery. You may use a drilling bit for metal, to break it like so:

![image](https://github.com/user-attachments/assets/adc75776-ab0d-42fa-a1b1-9c41b950f295)

That's all for the drilling. Now solder two leads to the solder points, pass them through the shafts,
and solder their other ends to the coin battery holder glued on the top:

![image](https://github.com/user-attachments/assets/55c8da96-430e-4a56-99ba-9ebd4d30dbf9)
![image](https://github.com/user-attachments/assets/732d000a-8d09-4e43-b86f-53d78764601f)

That's all and thank you for reading.
