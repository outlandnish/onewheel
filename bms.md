---
title: BMS Info
subtitle: BMS for both XR and Pint.
layout: page
show_sidebar: false
---

## BMS

#### +XR, HW: 4209, PCB v2.0.5

![](images/bms_xr_2.0.5.jpg)

* `PIC16F1788-I/ML` RISC CPU
  * Datasheet: [40001675C.pdf](assets/40001675C.pdf)
  * this one sits in between the `MAX14921`'s SPI interface and exposed contacts on the PCB
  * [https://www.digikey.com/products/en?KeyWords=PIC16F1788-I/ML](https://www.digikey.com/products/en?KeyWords=PIC16F1788-I/ML)
  * ![](images/bms_xr_2.0.5_16f1788.jpg)
* `PROG1` pinout:
  * ![](images/bms_xr_2.0.5_PROG1.png)  
* `MAX14921` battery measurement analog front-end
  * controlled by an SPI interface
  * Datasheet: [MAX14920-MAX14921.pdf](assets/MAX14920-MAX14921.pdf)
  * ![](images/bms_xr_2.0.5_max14921.jpg)
* `020N08N5` MOSFET
  * Datasheet: [Infineon-IPB020N08N5-DS-v02_02-EN.pdf](assets/Infineon-IPB020N08N5-DS-v02_02-EN.pdf)
  * [https://www.digikey.com/en/products/detail/infineon-technologies/IPB020N08N5ATMA1/5960189](https://www.digikey.com/en/products/detail/infineon-technologies/IPB020N08N5ATMA1/5960189)
  * ![](images/bms_xr_2.0.5_020n08n5.jpg)
* `CSD19536KTT` power MOSFET
  * Datasheet: [csd19536ktt.pdf](assets/csd19536ktt.pdf)
  * [https://www.digikey.com/en/products/detail/texas-instruments/CSD19536KTT/5215835](https://www.digikey.com/en/products/detail/texas-instruments/CSD19536KTT/5215835)
  * ![](images/bms_xr_2.0.5_csd19536ktt.jpg)
* `LM393-N` voltage comparator
  * Datasheet: [lm393-n.pdf](assets/lm393-n.pdf)
  * ![](images/bms_xr_2.0.5_lm393.jpg)
* `VP1786` (`SN65HVD1786D`) transceiver
  * Datasheet: [sn65hvd1791.pdf](assets/sn65hvd1791.pdf)
  * ![](images/bms_xr_2.0.5_vp1786.jpg)
* `3920R 1L00 1% 1846` current sense resistor
  * Datasheet: [2629492.pdf](assets/2629492.pdf)
  * ![](images/bms_xr_2.0.5_3920r.jpg)

### Connectors
* Amass XT60PW connectors for battery / controller power (note reversed polarity for battery connector)
* JAE ES9 female (on PCB) / male (on wire) connector for charger cable
  * [https://www.digikey.com/catalog/en/partgroup/es9-series/47166](https://www.digikey.com/catalog/en/partgroup/es9-series/47166)
  * [https://www.digikey.com/catalog/en/partgroup/es9-series/47164](https://www.digikey.com/catalog/en/partgroup/es9-series/47164)
* JST GH 5-position female header used for connector to controller
  * [https://www.digikey.com/en/products/detail/jst-sales-america-inc/BM05B-GHS-TBT-LF-SN-N/807803](https://www.digikey.com/en/products/detail/jst-sales-america-inc/BM05B-GHS-TBT-LF-SN-N/807803)

## Hardware version and PCB revision combinations

Note: This is based on very small sample size. (Currently about 10 boards.)

### +XR

| Hardware version | BMS PCB revision | Controller PCB revision |
|------------------|------------------|-------------------------|
| 4209             | v2.0.4 - v2.0.5  | r2.9                    |
| 4210             | v2.0.7           | ?                       |

### Pint

| Hardware version | BMS PCB revision | Controller PCB revision |
|------------------|------------------|-------------------------|
| 5300             | v2.0.7           | r3.1.3                  |
| 5314             | v2.0.7           | ?                       |

## Balance port pinout

Close-up of the BMS connector pinout and the XT-60 connector

![](images/bms_pinout.png)

Each pack has 4 10k NTC Thermistors placed in-between cells for temperature monitoring.
