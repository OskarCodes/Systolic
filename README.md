# Systolic
Altium Designer files for my electrocardiogram (ECG): Systolic.
![Picture showing Systolic](docs/images/ECG.jpg)
## What is Systolic?
Systolic is a project I have been working on for a couple months. It is an ultra-low-cost ECG which one day I hope can be used in developing countries. Systolic is very compact, and only requires a host device (e.g. a laptop). On the host device, a [program]( https://github.com/OskarCodes/SystolicHost) I made runs and allows for the configuration of sampling settings, starting/stopping sampling, and finally, the parsing of results. Systolic currently costs roughly 55 USD per unit (for 100).

## Briefly, how does it work?
Systolic uses an ADS1293 from Texas Instruments with an STM32L475 microcontroller. They communicate over SPI, and the STM32 then transfers this data to the host device over a USB virtual com port.

## What are the results like?
Take a look, they're awesome, in my opinion!

![ECG Sample was taken at 533 Hz](docs/images/ecg_sample_533hz.jpg)
This sample was taken at 533 Hz. Compared to the other sample taken at 133 Hz in the docs/image folder, it has more noise.

## Setup
```shell
git clone https://github.com/OskarCodes/Systolic.git
cd Systolic/
```
And you are done! The project can then be opened up in Altium.

## Contributing
I immensely appreciate any contribution to this project, no matter the size. Please feel free to make a pull request! If you have any questions, please do not hesitate to reach out.

## Extremely important
This device is not medically certified, nor is it in its current state intended for use in diagnosis/treatment of any medical conditions. Although it may not have harmed me during my testing so far, that does not mean that it is safe. 
If you really want to make this ECG, remember that you are have been warned about the potential risks. I assume no liability for any harm or damage from the use of this device. 
## Licensing
This project is licensed under the GPL-3.0 license. I chose this because I want all changes to Systolic and supporting software, no matter who by, to be accessible to everyone.
