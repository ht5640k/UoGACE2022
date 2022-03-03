# **Machine Vision Foam Dart Turret**

### **UoG Advanced Computer Engineering Project 2021/22**
<br>

## **About the Project**

This project has been developed by the contributors below as a submission of coursework for the University of Greenwich Advanced Computer Engineering Module, academic year 2021/22.

The Machine Vision Foam Dart Turret is a fully automated object targetting system designed to identify, target, and shoot (with a foam dart to two) a person not recognised by the machine vision. It features a 12 dart magazine, 2 axis movement, a Jetson Nano controlled vision system, and two interfaces (one for LAN based web control and video feedback, and one for automatic downloading of this GitHub repo).

Mechanical parts of this project are mostly custom using standard industry parts for difficult to manufacture parts such as stepper motors and bearings. The software is written mostly from scratch, using part libraries where sensible, particularily for the arduino interfacing with hardware, and the Jetson managing its machine vision identification.

![System block diagram](https://raw.githubusercontent.com/vinthund/UoGACE2022/ad4646d/System%20Documentation/System_Block_Diagram.png)
*System Concept Block Diagram*

## **Contributors**

- [Andrew Dean - ad4646d](https://www.github.com/ad4646d)
- [Chris Halsall - ch6941r -](https://www.github.com/ch6941r)  [AfterEarthLtd](https://www.github.com/AfterEarthLTD)
- [vinthund](https://www.github.com/vinthund)
- [ht5640k](https://www.github.com/ht5640k)
- [JoelSmalls](https://www.github.com/JoelSmalls)
- [kamyar123](https://www.github.com/kamyar123)
- [rowBoat](https://www.github.com/rowboat)
<br>


## **Firing Mechanism Mechanical Design** - [Chris Halsall - ch6941r](https://www.github.com/ch6941r)

The firing mechanism contains a few pre-made parts including a small stepper motor, the firing motors and barrel, a servo, and a bearing. All other parts have been designed in Fusion 360 and printed in orange PLA on an Ender 3 FDM 3D printer. It features a 12 dart rotary magazine driven by the stepper motor from one end and supported by a bearing at the other end. Through the bearing is mounted a magnet and a magnetic position sensor so that the control electronics can measure the angle of the magazine. A servo is mounted in the base and, with a custom arm, is capable of pushing a dart from the magazine into the firing motors and thus propelling it out of the barrel. A mounting plate is attached to the front of the design to securely mount the camera for machine vision. Finally, a hole and hex slot has been designed in to allow for easy mounting to the pan/tilt mehcanism.
<br>
<br>

## **Pan-Tilt Mechanism Mechanical Design** - [Andrew Dean - ad4646d](https://www.github.com/ad4646d)

The [pan-tilt mechanism](https://github.com/vinthund/UoGACE2022/tree/main/Pan-TiltAssembly) is a bespoke 3D printed mechanism that was designed in tandem with bespoke the [firing mechanism](https://github.com/vinthund/UoGACE2022/tree/ad4646d/3D%20Designs/Firing%20Mech) using AutoDesk Fusion 360.

***{insert up-to-date photo}***

Herringbone gears were chosen for both pan and tilt axes for a number of reasons:
* They feature minimal backlash compared to 3D printed spur gears
* They are quieter in operation compared to 3D printed spur gears
* More torque can be transmitted through them vs 3D printed spur gears\

A gearing ratio of 4:1 was chosen to increase the torque output of the NEMA17 steppers and to give greater step-angle resolution... ***add further calculations for speed and torque output***.

All bespoke 3D printed parts for the pan-tilt mechanism were printed in black PLA using an Anycubic i3 Mega.

NEMA17 stepper motors were chosen as they provided adequate torque output to move both axes, they also feature a step angle of 1.8˚.
* A [NEMA17x34](https://www.omc-stepperonline.com/nema-17-bipolar-1-8deg-26ncm-36-8oz-in-0-4a-12v-42x42x34mm-4-wires.html?search=17hs13) was chosen for the tilt axis
* A [NEMA17x39](https://www.omc-stepperonline.com/nema-17-bipolar-45ncm-6374ozin-15a-42x42x39mm-4-wires-w--1m-pin-connector.html?search=17HS15-1504S-X1&description=true) was chosen for the pan axis

[A4988 stepper drivers](https://www.amazon.co.uk/gp/product/B07MXXL2KW) were selected for a number of reasons:
* They can drive bi-polar stepper motors up to 2A/phase
* They only require two control pins from the microcontroller to control steps and direction
* They are still readily available amidst the current global component shortage

A combination of [small neodymium magnets](https://www.first4magnets.com/circular-disc-rod-c34/2mm-dia-x-2mm-thick-n42sh-neodymium-magnet-0-15kg-pull-p3327#ps_0_3379|ps_1_16690) and [hall effect sensors](https://www.amazon.co.uk/gp/product/B08QCRYXPK) are used to both 'home' each axis and to limit their movement, these were chosen over limit switches as they simplified mechanical assembly and design.

An [off-the-shelf electronics enclosure](https://www.screwfix.com/p/schneider-electric-ip66-weatherproof-outdoor-enclosure-164-x-105-x-192mm/) was chosen to be the base of the system, this particular enclosure was chosen as it would provide adequate space to house all system components.

A [lazy susan bearing](https://www.stilesandbates.co.uk/75mm-square-lazy-susan-bearing-1709.php) was chosen for the pan axis as it allowed for a convenient way to manage cables between the combined pan-tilt/firing mech and their control electronics in the enclosure below.

The full parts list for the pan-tilt mechanism can be found [here](https://github.com/vinthund/UoGACE2022/blob/ad4646d/Pan-TiltAssembly/Documentation/Pan-Tilt%20Head%20Parts%20List.pdf).\
STEP files for the pan-tilt mechanism can be found [here](https://github.com/vinthund/UoGACE2022/tree/main/Pan-TiltAssembly/CAD_Files).

<br>


## **Firing Mechanism Communications** - [JoelSmalls](https://www.github.com/JoelSmalls)

***Add your summary of work here and delete this comment.***

<br>

## **Pan/Tilt Mechanism Communicatons** - [ht5640k](https://www.github.com/ht5640k)

***Add your summary of work here and delete this comment.***

<br>

## **Machine Vision Target Aquisition** - [vinthund](https://www.github.com/vinthund)

***Add your summary of work here and delete this comment.***

<br>

## **Web Server and Website** - [rowBoat](https://www.github.com/rowboat)

***Add your summary of work here and delete this comment.***

<br>

## **Android App** - [kamyar123](https://www.github.com/kamyar123)

***Add your summary of work here and delete this comment.***

<br>

## **Project Management** - [Andrew Dean - ad4646d](https://www.github.com/ad4646d) & [Chris Halsall - ch6941r](https://www.github.com/ch6941r)

***Add your summary of work here and delete this comment.***

<br>

## **GitHub Management** - [vinthund](https://www.github.com/vinthund)

***Add your summary of work here and delete this comment.***

<br>

# **License**

Due to the sensitive nature of projectile firing technology, much thought has gone into the ethics of releasing a publically available repository with details of how the project was created. Please note that the content contained within this repository should be used solely for EDUCSTION purposes. For full details please see the [License](LICENSE) document found in the root of this repository. This license has been based upon the MIT license.