# ดาวและกลุ่มดาวในสคริปต์ stargazer

สร้างจาก `shared/catalog.lua` เมื่อ 2026-10-11 ถ้าแก้แคตตาล็อกแล้ว ตัวเลขในไฟล์นี้จะไม่ตรง

## สรุป

| รายการ | จำนวน |
| --- | ---: |
| ดาวจริงในแคตตาล็อก | **470 ดวง** |
| ดาวพื้นหลังสุ่ม (ไม่ใช่ดาวจริง ไม่มีชื่อ ตั้งที่ `Config.Sky.starCount`) | 420 ดวง |
| ดาวทั้งหมดบนฟ้า | 890 ดวง |
| กลุ่มดาว | **62 กลุ่ม** (วาดเส้นเอง 12, กลุ่มดาวสากล IAU 50) |
| เส้นที่ต้องลากรวมทุกกลุ่ม | 461 เส้น |
| วัตถุสำหรับเกมปรับโฟกัส | 8 ชิ้น (ดาวเคราะห์ 2, วัตถุห้วงอวกาศลึก 6) |
| รายการในสมุดดาว | 70 (กลุ่มดาว 62 + วัตถุ 8) |

ดาวในแคตตาล็อก

- ตั้งชื่อตาม IAU 246 ดวง, Bayer (เช่น `mu_and` = μ And) 193 ดวง, Flamsteed (เช่น `f41_ari` = 41 Ari) 23 ดวง, เลข Hipparcos (เช่น `hip30665` = HIP 30665) 8 ดวง
- สว่างที่สุด Sirius (`sirius`) โชติมาตร -1.46, จางที่สุด HIP 30665 (`hip30665`) โชติมาตร 6.60
- โชติมาตร: ต่ำกว่า 1 = 10, 1-2 = 22, 2-3 = 84, 3-4 = 170, 4-5 = 160, 5 ขึ้นไป = 24 ดวง
- สี: ฟ้าขาว 113, ขาว 101, ขาวเหลือง 75, ส้ม 143, ส้มแดง 38 ดวง
- อยู่ในกลุ่มดาว 463 ดวง, ไม่อยู่ในกลุ่มไหน 7 ดวง, อยู่มากกว่า 1 กลุ่ม 15 ดวง

ที่มาของข้อมูล

- 12 กลุ่มแรก (กระบวยใหญ่ ถึง หมาใหญ่) วาดเส้นเองแบบย่อ บางกลุ่มเป็นกลุ่มดาวย่อย (asterism) ไม่ใช่กลุ่มดาว IAU เช่น กระบวยใหญ่ สามเหลี่ยมฤดูร้อน จัตุรัสม้าบิน
- 50 กลุ่มที่เหลือเป็นกลุ่มดาวสากล IAU เส้นตาม Stellarium (sky culture `modern`) ตำแหน่งและโชติมาตรจาก Hipparcos
- ไม่มีกลุ่มดาวฟ้าใต้ 30 กลุ่ม (เช่น กางเขนใต้ คนครึ่งม้า อีริดานัส) เพราะที่ละติจูด 34° ดาวบางดวงในกลุ่มไม่ขึ้นพ้นขอบฟ้า 6°
- งู (Serpens) แยกเป็น 2 กลุ่ม คือส่วนหัวกับส่วนหาง

## กลุ่มดาวทั้งหมด

ละติจูด 34° (Los Santos) คอลัมน์ "สูงสุด" คือมุมเงยของใจกลางกลุ่มตอนขึ้นสูงสุด
"ตามหา" = ใจกลางขึ้นถึง 18° และดาวทุกดวงพ้นขอบฟ้า 6° ได้ในบางช่วง, "ลากเส้น" = ใจกลางขึ้นถึง 22°
"กลางฟ้าเที่ยงคืน" = เดือนที่กลุ่มอยู่สูงสุดตอนเที่ยงคืน (ฟ้าในเกมตามวันที่จริงของเครื่องเซิร์ฟ)

| # | ชื่อไทย | อังกฤษ | key | ดาว | เส้น | สูงสุด | ตามหา | ลากเส้น | กลางฟ้าเที่ยงคืน |
| ---: | --- | --- | --- | ---: | ---: | ---: | :---: | :---: | --- |
| 1 | กระบวยใหญ่ | Big Dipper | `big_dipper` | 7 | 7 | 67° | ✓ | ✓ | มี.ค. |
| 2 | กระบวยเล็ก | Little Dipper | `little_dipper` | 7 | 7 | 44° | ✓ | ✓ | พ.ค. |
| 3 | แคสซิโอเปีย | Cassiopeia | `cassiopeia` | 5 | 4 | 64° | ✓ | ✓ | ต.ค. |
| 4 | หงส์ | Cygnus | `cygnus` | 5 | 4 | 85° | ✓ | ✓ | ก.ค. |
| 5 | สามเหลี่ยมฤดูร้อน | Summer Triangle | `summer_triangle` | 3 | 3 | 88° | ✓ | ✓ | ก.ค. |
| 6 | นายพราน | Orion | `orion` | 8 | 8 | 56° | ✓ | ✓ | ธ.ค. |
| 7 | วัว | Taurus | `taurus` | 7 | 6 | 75° | ✓ | ✓ | ธ.ค. |
| 8 | คนคู่ | Gemini | `gemini` | 6 | 5 | 81° | ✓ | ✓ | ม.ค. |
| 9 | สิงโต | Leo | `leo` | 9 | 9 | 75° | ✓ | ✓ | ก.พ. |
| 10 | จัตุรัสม้าบิน | Great Square | `pegasus` | 4 | 4 | 78° | ✓ | ✓ | ก.ย. |
| 11 | คนเลี้ยงสัตว์ | Boötes | `bootes` | 6 | 6 | 86° | ✓ | ✓ | เม.ย. |
| 12 | หมาใหญ่ | Canis Major | `canis_major` | 5 | 4 | 32° | ✓ | ✓ | ม.ค. |
| 13 | แอนดรอมิดา | Andromeda | `andromeda` | 6 | 5 | 87° | ✓ | ✓ | ต.ค. |
| 14 | เครื่องสูบลม | Antlia | `antlia` | 2 | 1 | 22° | ✓ | ✓ | ก.พ. |
| 15 | คนแบกหม้อน้ำ | Aquarius | `aquarius` | 15 | 14 | 47° | ✓ | ✓ | ส.ค. |
| 16 | นกอินทรี | Aquila | `aquila` | 9 | 8 | 62° | ✓ | ✓ | ก.ค. |
| 17 | แกะ | Aries | `aries` | 4 | 3 | 79° | ✓ | ✓ | ต.ค. |
| 18 | สารถี | Auriga | `auriga` | 6 | 6 | 85° | ✓ | ✓ | ธ.ค. |
| 19 | ยีราฟ | Camelopardalis | `camelopardalis` | 5 | 5 | 56° | ✓ | ✓ | พ.ย. |
| 20 | ปู | Cancer | `cancer` | 6 | 5 | 75° | ✓ | ✓ | ม.ค. |
| 21 | หมาล่าเนื้อ | Canes Venatici | `canes_venatici` | 2 | 1 | 84° | ✓ | ✓ | เม.ย. |
| 22 | หมาเล็ก | Canis Minor | `canis_minor` | 2 | 1 | 63° | ✓ | ✓ | ม.ค. |
| 23 | แพะทะเล | Capricornus | `capricornus` | 9 | 9 | 37° | ✓ | ✓ | ส.ค. |
| 24 | ซีฟิอัส | Cepheus | `cepheus` | 5 | 6 | 57° | ✓ | ✓ | ส.ค. |
| 25 | ปลาวาฬ | Cetus | `cetus` | 19 | 20 | 52° | ✓ | ✓ | ต.ค. |
| 26 | นกพิราบ | Columba | `columba` | 7 | 6 | 20° | ✓ | ✗ | ธ.ค. |
| 27 | ผมเบเรนิซ | Coma Berenices | `coma_berenices` | 3 | 2 | 81° | ✓ | ✓ | เม.ย. |
| 28 | มงกุฎเหนือ | Corona Borealis | `corona_borealis` | 7 | 6 | 84° | ✓ | ✓ | พ.ค. |
| 29 | อีกา | Corvus | `corvus` | 6 | 6 | 36° | ✓ | ✓ | มี.ค. |
| 30 | ถ้วย | Crater | `crater` | 8 | 9 | 40° | ✓ | ✓ | มี.ค. |
| 31 | โลมา | Delphinus | `delphinus` | 5 | 5 | 71° | ✓ | ✓ | ก.ค. |
| 32 | มังกร | Draco | `draco` | 15 | 15 | 57° | ✓ | ✓ | มิ.ย. |
| 33 | ม้าน้อย | Equuleus | `equuleus` | 4 | 4 | 64° | ✓ | ✓ | ส.ค. |
| 34 | เตาไฟ | Fornax | `fornax` | 2 | 1 | 25° | ✓ | ✓ | พ.ย. |
| 35 | เฮอร์คิวลีส | Hercules | `hercules` | 18 | 18 | 90° | ✓ | ✓ | มิ.ย. |
| 36 | งูไฮดรา | Hydra | `hydra` | 25 | 25 | 42° | ✓ | ✓ | ก.พ. |
| 37 | กิ้งก่า | Lacerta | `lacerta` | 6 | 6 | 77° | ✓ | ✓ | ส.ค. |
| 38 | สิงโตเล็ก | Leo Minor | `leo_minor` | 4 | 4 | 88° | ✓ | ✓ | ก.พ. |
| 39 | กระต่าย | Lepus | `lepus` | 13 | 14 | 39° | ✓ | ✓ | ธ.ค. |
| 40 | คันชั่ง | Libra | `libra` | 5 | 5 | 39° | ✓ | ✓ | พ.ค. |
| 41 | แมวป่า | Lynx | `lynx` | 8 | 7 | 78° | ✓ | ✓ | ม.ค. |
| 42 | พิณ | Lyra | `lyra` | 5 | 5 | 88° | ✓ | ✓ | ก.ค. |
| 43 | กล้องจุลทรรศน์ | Microscopium | `microscopium` | 3 | 2 | 23° | ✓ | ✓ | ส.ค. |
| 44 | ม้ายูนิคอร์น | Monoceros | `monoceros` | 11 | 11 | 57° | ✓ | ✓ | ม.ค. |
| 45 | คนแบกงู | Ophiuchus | `ophiuchus` | 7 | 7 | 52° | ✓ | ✓ | มิ.ย. |
| 46 | ม้าบิน | Pegasus | `pegasus_full` | 14 | 14 | 77° | ✓ | ✓ | ส.ค. |
| 47 | เพอร์ซิอัส | Perseus | `perseus` | 11 | 10 | 82° | ✓ | ✓ | พ.ย. |
| 48 | ปลาคู่ | Pisces | `pisces` | 20 | 21 | 65° | ✓ | ✓ | ก.ย. |
| 49 | ปลาใต้ | Piscis Austrinus | `piscis_austrinus` | 7 | 6 | 25° | ✓ | ✓ | ส.ค. |
| 50 | เข็มทิศ | Pyxis | `pyxis` | 3 | 2 | 24° | ✓ | ✓ | ม.ค. |
| 51 | ลูกศร | Sagitta | `sagitta` | 5 | 4 | 75° | ✓ | ✓ | ก.ค. |
| 52 | คนยิงธนู | Sagittarius | `sagittarius` | 21 | 24 | 27° | ✓ | ✓ | ก.ค. |
| 53 | แมงป่อง | Scorpius | `scorpius` | 13 | 12 | 22° | ✓ | ✗ | มิ.ย. |
| 54 | ช่างแกะสลัก | Sculptor | `sculptor` | 3 | 3 | 22° | ✓ | ✓ | ก.ย. |
| 55 | โล่ | Scutum | `scutum` | 5 | 5 | 46° | ✓ | ✓ | ก.ค. |
| 56 | งู (ส่วนหัว) | Serpens Caput | `serpens_caput` | 8 | 8 | 64° | ✓ | ✓ | พ.ค. |
| 57 | งู (ส่วนหาง) | Serpens Cauda | `serpens_cauda` | 8 | 7 | 49° | ✓ | ✓ | มิ.ย. |
| 58 | เครื่องวัดมุม | Sextans | `sextans` | 2 | 1 | 57° | ✓ | ✓ | ก.พ. |
| 59 | สามเหลี่ยม | Triangulum | `triangulum` | 3 | 3 | 89° | ✓ | ✓ | ต.ค. |
| 60 | หมีใหญ่ | Ursa Major | `ursa_major` | 18 | 19 | 69° | ✓ | ✓ | มี.ค. |
| 61 | หญิงสาว | Virgo | `virgo` | 12 | 12 | 55° | ✓ | ✓ | เม.ย. |
| 62 | หมาจิ้งจอก | Vulpecula | `vulpecula` | 2 | 1 | 82° | ✓ | ✓ | ก.ค. |

เล่นเกมตามหาได้ 62 กลุ่ม, เกมลากเส้นได้ 60 กลุ่ม

## ดาวในแต่ละกลุ่ม

เรียงตามลำดับใน `stars` ของกลุ่ม ดาวที่มี * อยู่มากกว่า 1 กลุ่ม

### 1. กระบวยใหญ่ (Big Dipper)

`big_dipper` ดาว 7 ดวง เส้น 7 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Dubhe * | `dubhe` | 1.80 | ส้ม |
| Merak * | `merak` | 2.40 | ขาว |
| Phecda * | `phecda` | 2.40 | ขาว |
| Megrez * | `megrez` | 3.30 | ขาว |
| Alioth * | `alioth` | 1.80 | ขาว |
| Mizar * | `mizar` | 2.20 | ขาว |
| Alkaid * | `alkaid` | 1.90 | ฟ้าขาว |

### 2. กระบวยเล็ก (Little Dipper)

`little_dipper` ดาว 7 ดวง เส้น 7 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Polaris | `polaris` | 2.00 | ขาวเหลือง |
| Yildun | `yildun` | 4.40 | ขาว |
| ε UMi | `eps_umi` | 4.20 | ขาวเหลือง |
| ζ UMi | `zeta_umi` | 4.30 | ขาว |
| η UMi | `eta_umi` | 4.90 | ขาว |
| Pherkad | `pherkad` | 3.00 | ขาว |
| Kochab | `kochab` | 2.10 | ส้ม |

### 3. แคสซิโอเปีย (Cassiopeia)

`cassiopeia` ดาว 5 ดวง เส้น 4 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Caph | `caph` | 2.30 | ขาวเหลือง |
| Schedar | `schedar` | 2.20 | ส้ม |
| γ Cas | `gamma_cas` | 2.40 | ฟ้าขาว |
| Ruchbah | `ruchbah` | 2.70 | ขาว |
| Segin | `segin` | 3.40 | ฟ้าขาว |

### 4. หงส์ (Cygnus)

`cygnus` ดาว 5 ดวง เส้น 4 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Deneb * | `deneb` | 1.25 | ขาว |
| Sadr | `sadr` | 2.20 | ขาวเหลือง |
| Albireo | `albireo` | 3.10 | ส้ม |
| Gienah | `gienah` | 2.50 | ส้ม |
| δ Cyg | `delta_cyg` | 2.90 | ฟ้าขาว |

### 5. สามเหลี่ยมฤดูร้อน (Summer Triangle)

`summer_triangle` ดาว 3 ดวง เส้น 3 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Vega * | `vega` | 0.03 | ฟ้าขาว |
| Deneb * | `deneb` | 1.25 | ขาว |
| Altair * | `altair` | 0.77 | ขาว |

### 6. นายพราน (Orion)

`orion` ดาว 8 ดวง เส้น 8 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Betelgeuse | `betelgeuse` | 0.50 | ส้มแดง |
| Bellatrix | `bellatrix` | 1.60 | ฟ้าขาว |
| Meissa | `meissa` | 3.40 | ฟ้าขาว |
| Alnitak | `alnitak` | 1.80 | ฟ้าขาว |
| Alnilam | `alnilam` | 1.70 | ฟ้าขาว |
| Mintaka | `mintaka` | 2.20 | ฟ้าขาว |
| Saiph | `saiph` | 2.10 | ฟ้าขาว |
| Rigel | `rigel` | 0.13 | ฟ้าขาว |

### 7. วัว (Taurus)

`taurus` ดาว 7 ดวง เส้น 6 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Aldebaran | `aldebaran` | 0.85 | ส้ม |
| Elnath * | `elnath` | 1.65 | ฟ้าขาว |
| ζ Tau | `zeta_tau` | 3.00 | ฟ้าขาว |
| γ Tau | `gamma_tau` | 3.65 | ขาวเหลือง |
| δ Tau | `delta_tau` | 3.80 | ขาวเหลือง |
| ε Tau | `eps_tau` | 3.50 | ส้ม |
| θ Tau | `theta_tau` | 3.40 | ขาว |

### 8. คนคู่ (Gemini)

`gemini` ดาว 6 ดวง เส้น 5 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Castor | `castor` | 1.60 | ขาว |
| Pollux | `pollux` | 1.15 | ส้ม |
| Alhena | `alhena` | 1.90 | ขาว |
| Mebsuta | `mebsuta` | 3.00 | ขาวเหลือง |
| Tejat | `tejat` | 2.90 | ส้มแดง |
| Wasat | `wasat` | 3.50 | ขาว |

### 9. สิงโต (Leo)

`leo` ดาว 9 ดวง เส้น 9 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Regulus | `regulus` | 1.35 | ฟ้าขาว |
| η Leo | `eta_leo` | 3.50 | ขาว |
| Algieba | `algieba` | 2.00 | ส้ม |
| Adhafera | `adhafera` | 3.40 | ขาว |
| Rasalas | `rasalas` | 3.90 | ส้ม |
| ε Leo | `eps_leo` | 3.00 | ขาวเหลือง |
| Denebola | `denebola` | 2.10 | ขาว |
| Zosma | `zosma` | 2.55 | ขาว |
| Chertan | `chertan` | 3.30 | ขาว |

### 10. จัตุรัสม้าบิน (Great Square)

`pegasus` ดาว 4 ดวง เส้น 4 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Markab * | `markab` | 2.50 | ฟ้าขาว |
| Scheat * | `scheat` | 2.40 | ส้มแดง |
| Alpheratz * | `alpheratz` | 2.10 | ฟ้าขาว |
| Algenib * | `algenib` | 2.80 | ฟ้าขาว |

### 11. คนเลี้ยงสัตว์ (Boötes)

`bootes` ดาว 6 ดวง เส้น 6 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Arcturus | `arcturus` | -0.05 | ส้ม |
| Izar | `izar` | 2.40 | ส้ม |
| δ Boo | `delta_boo` | 3.50 | ขาวเหลือง |
| Nekkar | `nekkar` | 3.50 | ขาวเหลือง |
| Seginus | `seginus` | 3.00 | ขาว |
| Muphrid | `muphrid` | 2.70 | ขาวเหลือง |

### 12. หมาใหญ่ (Canis Major)

`canis_major` ดาว 5 ดวง เส้น 4 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Sirius | `sirius` | -1.46 | ฟ้าขาว |
| Mirzam | `mirzam` | 2.00 | ฟ้าขาว |
| Adhara | `adhara` | 1.50 | ฟ้าขาว |
| Wezen | `wezen` | 1.80 | ขาวเหลือง |
| Aludra | `aludra` | 2.45 | ฟ้าขาว |

### 13. แอนดรอมิดา (Andromeda)

`andromeda` ดาว 6 ดวง เส้น 5 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Alpheratz * | `alpheratz` | 2.10 | ฟ้าขาว |
| δ And | `delta_and` | 3.27 | ส้ม |
| Mirach | `mirach` | 2.07 | ส้มแดง |
| Almach | `almach` | 2.10 | ส้ม |
| μ And | `mu_and` | 3.86 | ขาว |
| ν And | `nu_and` | 4.53 | ฟ้าขาว |

### 14. เครื่องสูบลม (Antlia)

`antlia` ดาว 2 ดวง เส้น 1 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| α Ant | `alpha_ant` | 4.28 | ส้ม |
| η Ant | `eta_ant` | 5.23 | ขาวเหลือง |

### 15. คนแบกหม้อน้ำ (Aquarius)

`aquarius` ดาว 15 ดวง เส้น 14 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Sadalsuud | `sadalsuud` | 2.90 | ส้ม |
| Sadalmelik | `sadalmelik` | 2.95 | ส้ม |
| Sadachbia | `sadachbia` | 3.86 | ฟ้าขาว |
| Sadaltager | `sadaltager` | 3.65 | ขาวเหลือง |
| η Aqr | `eta_aqr` | 4.04 | ฟ้าขาว |
| Hydor | `hydor` | 3.73 | ส้มแดง |
| ψ¹ Aqr | `psi1_aqr` | 4.24 | ส้ม |
| b¹ Aqr | `b1_aqr` | 3.96 | ส้ม |
| Ancha | `ancha` | 4.17 | ส้ม |
| ι Aqr | `iota_aqr` | 4.29 | ฟ้าขาว |
| σ Aqr | `sigma_aqr` | 4.82 | ฟ้าขาว |
| τ² Aqr | `tau2_aqr` | 4.05 | ส้มแดง |
| Skat | `skat` | 3.27 | ขาว |
| c² Aqr | `c2_aqr` | 3.68 | ส้ม |
| Albali | `albali` | 3.78 | ขาว |

### 16. นกอินทรี (Aquila)

`aquila` ดาว 9 ดวง เส้น 8 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Alshain | `alshain` | 3.71 | ส้ม |
| Altair * | `altair` | 0.77 | ขาว |
| Tarazed | `tarazed` | 2.72 | ส้มแดง |
| Almizan | `almizan` | 3.36 | ขาวเหลือง |
| η Aql | `eta_aql` | 3.87 | ขาวเหลือง |
| θ Aql | `theta_aql` | 3.24 | ฟ้าขาว |
| Okab | `okab` | 2.99 | ขาว |
| Deneb al Okab Borealis | `deneb_al_okab_borealis` | 4.02 | ส้ม |
| Al Thalimain Prior | `al_thalimain_prior` | 3.43 | ฟ้าขาว |

### 17. แกะ (Aries)

`aries` ดาว 4 ดวง เส้น 3 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Bharani | `bharani` | 3.61 | ฟ้าขาว |
| Hamal | `hamal` | 2.01 | ส้ม |
| Sheratan | `sheratan` | 2.64 | ขาว |
| Mesarthim | `mesarthim` | 3.88 | ฟ้าขาว |

### 18. สารถี (Auriga)

`auriga` ดาว 6 ดวง เส้น 6 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Mahasim | `mahasim` | 2.65 | ฟ้าขาว |
| Menkalinan | `menkalinan` | 1.90 | ขาว |
| Capella | `capella` | 0.08 | ขาวเหลือง |
| Saclateni | `saclateni` | 3.69 | ส้ม |
| Hassaleh | `hassaleh` | 2.69 | ส้มแดง |
| Elnath * | `elnath` | 1.65 | ฟ้าขาว |

### 19. ยีราฟ (Camelopardalis)

`camelopardalis` ดาว 5 ดวง เส้น 5 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| HIP 16228 | `hip16228` | 4.21 | ขาวเหลือง |
| HIP 18505 | `hip18505` | 4.95 | ฟ้าขาว |
| α Cam | `alpha_cam` | 4.26 | ฟ้าขาว |
| γ Cam | `gamma_cam` | 4.59 | ขาว |
| HIP 25110 | `hip25110` | 5.08 | ขาวเหลือง |

### 20. ปู (Cancer)

`cancer` ดาว 6 ดวง เส้น 5 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Zubanah | `zubanah` | 4.03 | ส้ม |
| Asellus Borealis | `asellus_borealis` | 4.66 | ขาว |
| χ Cnc | `chi_cnc` | 5.13 | ขาวเหลือง |
| Asellus Australis | `asellus_australis` | 3.94 | ส้ม |
| Tarf | `tarf` | 3.53 | ส้มแดง |
| Acubens | `acubens` | 4.26 | ขาว |

### 21. หมาล่าเนื้อ (Canes Venatici)

`canes_venatici` ดาว 2 ดวง เส้น 1 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Chara | `chara` | 4.24 | ขาวเหลือง |
| Cor Caroli | `cor_caroli` | 2.89 | ฟ้าขาว |

### 22. หมาเล็ก (Canis Minor)

`canis_minor` ดาว 2 ดวง เส้น 1 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Procyon | `procyon` | 0.34 | ขาว |
| Gomeisa | `gomeisa` | 2.89 | ฟ้าขาว |

### 23. แพะทะเล (Capricornus)

`capricornus` ดาว 9 ดวง เส้น 9 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Algedi | `algedi` | 3.58 | ส้ม |
| Dabih | `dabih` | 3.05 | ขาวเหลือง |
| θ Cap | `theta_cap` | 4.08 | ฟ้าขาว |
| ι Cap | `iota_cap` | 4.28 | ส้ม |
| Nashira | `nashira` | 3.69 | ขาวเหลือง |
| Deneb Algedi | `deneb_algedi` | 2.85 | ขาว |
| Yen | `yen` | 3.77 | ส้ม |
| Wei | `wei` | 4.13 | ขาวเหลือง |
| ω Cap | `omega_cap` | 4.12 | ส้มแดง |

### 24. ซีฟิอัส (Cepheus)

`cepheus` ดาว 5 ดวง เส้น 6 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| ζ Cep | `zeta_cep` | 3.39 | ส้มแดง |
| ι Cep | `iota_cep` | 3.50 | ส้ม |
| Alfirk | `alfirk` | 3.23 | ฟ้าขาว |
| Alderamin | `alderamin` | 2.45 | ขาว |
| Errai | `errai` | 3.21 | ส้ม |

### 25. ปลาวาฬ (Cetus)

`cetus` ดาว 19 ดวง เส้น 20 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Al Kaff al Jidhmah | `al_kaff_al_jidhmah` | 4.36 | ส้ม |
| ξ² Cet | `xi2_cet` | 4.30 | ฟ้าขาว |
| τ Cet | `tau_cet` | 3.49 | ขาวเหลือง |
| Diphda | `diphda` | 2.04 | ส้ม |
| Deneb Kaitos Shemali | `deneb_kaitos_shemali` | 3.56 | ส้ม |
| Dheneb | `dheneb` | 3.46 | ส้ม |
| Al Naymat | `al_naymat` | 3.60 | ส้ม |
| Baten Kaitos | `baten_kaitos` | 3.74 | ส้ม |
| Sadr al Kaitos | `sadr_al_kaitos` | 4.88 | ฟ้าขาว |
| ε Cet | `eps_cet` | 4.83 | ขาวเหลือง |
| π Cet | `pi_cet` | 4.24 | ฟ้าขาว |
| σ Cet | `sigma_cet` | 4.74 | ขาวเหลือง |
| Mira | `mira` | 3.50 | ส้มแดง |
| δ Cet | `delta_cet` | 4.08 | ฟ้าขาว |
| Kaffaljidhma | `kaffaljidhma` | 3.47 | ขาว |
| Menkar | `menkar` | 2.54 | ส้มแดง |
| λ Cet | `lambda_cet` | 4.71 | ฟ้าขาว |
| μ Cet | `mu_cet` | 4.27 | ขาวเหลือง |
| ν Cet | `nu_cet` | 4.87 | ส้ม |

### 26. นกพิราบ (Columba)

`columba` ดาว 7 ดวง เส้น 6 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| δ Col | `delta_col` | 3.85 | ส้ม |
| κ Col | `kappa_col` | 4.37 | ส้ม |
| γ Col | `gamma_col` | 4.36 | ฟ้าขาว |
| Wazn | `wazn` | 3.12 | ส้ม |
| η Col | `eta_col` | 3.96 | ส้ม |
| Phact | `phact` | 2.65 | ฟ้าขาว |
| ε Col | `eps_col` | 3.86 | ส้ม |

### 27. ผมเบเรนิซ (Coma Berenices)

`coma_berenices` ดาว 3 ดวง เส้น 2 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Diadem | `diadem` | 4.32 | ขาวเหลือง |
| β Com | `beta_com` | 4.23 | ขาวเหลือง |
| Al Dafirah | `al_dafirah` | 4.35 | ส้ม |

### 28. มงกุฎเหนือ (Corona Borealis)

`corona_borealis` ดาว 7 ดวง เส้น 6 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| θ CrB | `theta_crb` | 4.14 | ฟ้าขาว |
| Nusakan | `nusakan` | 3.66 | ขาวเหลือง |
| Alphecca | `alphecca` | 2.22 | ขาว |
| γ CrB | `gamma_crb` | 3.81 | ขาว |
| δ CrB | `delta_crb` | 4.59 | ขาวเหลือง |
| ε CrB | `eps_crb` | 4.14 | ส้ม |
| ι CrB | `iota_crb` | 4.98 | ฟ้าขาว |

### 29. อีกา (Corvus)

`corvus` ดาว 6 ดวง เส้น 6 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| η Crv | `eta_crv` | 4.30 | ขาวเหลือง |
| Algorab | `algorab` | 2.94 | ฟ้าขาว |
| γ Crv | `gamma_crv` | 2.58 | ฟ้าขาว |
| Minkar | `minkar` | 3.02 | ส้ม |
| Alchiba | `alchiba` | 4.02 | ขาวเหลือง |
| Kraz | `kraz` | 2.65 | ส้ม |

### 30. ถ้วย (Crater)

`crater` ดาว 8 ดวง เส้น 9 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Alkes | `alkes` | 4.08 | ส้ม |
| Al Sharasif | `al_sharasif` | 4.46 | ขาว |
| γ Crt | `gamma_crt` | 4.06 | ขาว |
| Labr | `labr` | 3.56 | ส้ม |
| ε Crt | `eps_crt` | 4.81 | ส้มแดง |
| θ Crt | `theta_crt` | 4.70 | ฟ้าขาว |
| η Crt | `eta_crt` | 5.17 | ฟ้าขาว |
| ζ Crt | `zeta_crt` | 4.71 | ส้ม |

### 31. โลมา (Delphinus)

`delphinus` ดาว 5 ดวง เส้น 5 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Aldulfin | `aldulfin` | 4.03 | ฟ้าขาว |
| Rotanev | `rotanev` | 3.64 | ขาวเหลือง |
| Sualocin | `sualocin` | 3.77 | ฟ้าขาว |
| Al Salib | `al_salib` | 4.27 | ส้ม |
| Al Ukud | `al_ukud` | 4.43 | ขาวเหลือง |

### 32. มังกร (Draco)

`draco` ดาว 15 ดวง เส้น 15 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Grumium | `grumium` | 3.73 | ส้ม |
| Eltanin | `eltanin` | 2.24 | ส้มแดง |
| Rastaban | `rastaban` | 2.79 | ส้ม |
| Kuma | `kuma` | 4.86 | ขาว |
| Altais | `altais` | 3.07 | ส้ม |
| Tyl | `tyl` | 3.84 | ส้ม |
| τ Dra | `tau_dra` | 4.45 | ส้ม |
| Alahakan | `alahakan` | 3.55 | ขาวเหลือง |
| Aldhibah | `aldhibah` | 3.17 | ฟ้าขาว |
| Athebyne | `athebyne` | 2.73 | ส้ม |
| θ Dra | `theta_dra` | 4.01 | ขาวเหลือง |
| Edasich | `edasich` | 3.29 | ส้ม |
| Thuban | `thuban` | 3.67 | ฟ้าขาว |
| κ Dra | `kappa_dra` | 3.85 | ฟ้าขาว |
| Giausar | `giausar` | 3.82 | ส้มแดง |

### 33. ม้าน้อย (Equuleus)

`equuleus` ดาว 4 ดวง เส้น 4 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| γ Equ | `gamma_equ` | 4.70 | ขาว |
| δ Equ | `delta_equ` | 4.47 | ขาวเหลือง |
| β Equ | `beta_equ` | 5.16 | ขาว |
| Kitalpha | `kitalpha` | 3.92 | ขาวเหลือง |

### 34. เตาไฟ (Fornax)

`fornax` ดาว 2 ดวง เส้น 1 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| β For | `beta_for` | 4.45 | ส้ม |
| Dalim | `dalim` | 3.80 | ขาวเหลือง |

### 35. เฮอร์คิวลีส (Hercules)

`hercules` ดาว 18 ดวง เส้น 18 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| ι Her | `iota_her` | 3.82 | ฟ้าขาว |
| θ Her | `theta_her` | 3.86 | ส้ม |
| ρ Her | `rho_her` | 4.15 | ฟ้าขาว |
| e Her | `e_her` | 4.64 | ขาว |
| π Her | `pi_her` | 3.16 | ส้ม |
| η Her | `eta_her` | 3.48 | ส้ม |
| σ Her | `sigma_her` | 4.20 | ฟ้าขาว |
| τ Her | `tau_her` | 3.91 | ฟ้าขาว |
| χ Her | `chi_her` | 4.60 | ขาวเหลือง |
| Rutilicus | `rutilicus` | 2.81 | ขาวเหลือง |
| Kornephoros | `kornephoros` | 2.78 | ส้ม |
| γ Her | `gamma_her` | 3.74 | ขาว |
| ε Her | `eps_her` | 3.92 | ฟ้าขาว |
| Maasym | `maasym` | 4.41 | ส้ม |
| Sarin | `sarin` | 3.12 | ขาว |
| μ Her | `mu_her` | 3.42 | ขาวเหลือง |
| ξ Her | `xi_her` | 3.70 | ส้ม |
| ο Her | `omicron_her` | 3.84 | ฟ้าขาว |

### 36. งูไฮดรา (Hydra)

`hydra` ดาว 25 ดวง เส้น 25 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| η Hya | `eta_hya` | 4.30 | ฟ้าขาว |
| Minchir | `minchir` | 4.45 | ส้ม |
| Minazal | `minazal` | 4.14 | ขาว |
| Ashlesha | `ashlesha` | 3.38 | ขาวเหลือง |
| ρ Hya | `rho_hya` | 4.35 | ฟ้าขาว |
| ζ Hya | `zeta_hya` | 3.11 | ส้ม |
| θ Hya | `theta_hya` | 3.89 | ฟ้าขาว |
| τ² Hya | `tau2_hya` | 4.54 | ขาว |
| Ukdah | `ukdah` | 4.59 | ขาวเหลือง |
| Alphard | `alphard` | 1.99 | ส้ม |
| 26 Hya | `f26_hya` | 4.77 | ส้ม |
| κ Hya | `kappa_hya` | 5.07 | ฟ้าขาว |
| Zhang | `zhang` | 4.11 | ส้ม |
| λ Hya | `lambda_hya` | 3.61 | ส้ม |
| μ Hya | `mu_hya` | 3.83 | ส้มแดง |
| ν Hya | `nu_hya` | 3.11 | ส้ม |
| χ¹ Hya | `chi1_hya` | 4.92 | ขาวเหลือง |
| ξ Hya | `xi_hya` | 3.54 | ส้ม |
| β Hya | `beta_hya` | 4.29 | ฟ้าขาว |
| ψ Hya | `psi_hya` | 4.94 | ส้ม |
| γ Hya | `gamma_hya` | 2.99 | ส้ม |
| π Hya | `pi_hya` | 3.25 | ส้ม |
| 50 Hya | `f50_hya` | 5.07 | ส้ม |
| k Hya | `k_hya` | 4.78 | ส้ม |
| e Hya | `e_hya` | 4.42 | ส้ม |

### 37. กิ้งก่า (Lacerta)

`lacerta` ดาว 6 ดวง เส้น 6 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| 1 Lac | `f1_lac` | 4.14 | ส้ม |
| 6 Lac | `f6_lac` | 4.52 | ฟ้าขาว |
| 5 Lac | `f5_lac` | 4.34 | ส้มแดง |
| 4 Lac | `f4_lac` | 4.55 | ขาว |
| β Lac | `beta_lac` | 4.42 | ส้ม |
| α Lac | `alpha_lac` | 3.76 | ขาว |

### 38. สิงโตเล็ก (Leo Minor)

`leo_minor` ดาว 4 ดวง เส้น 4 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Praecipua | `praecipua` | 3.79 | ส้ม |
| β LMi | `beta_lmi` | 4.20 | ส้ม |
| 21 LMi | `f21_lmi` | 4.49 | ขาว |
| 10 LMi | `f10_lmi` | 4.54 | ส้ม |

### 39. กระต่าย (Lepus)

`lepus` ดาว 13 ดวง เส้น 14 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| θ Lep | `theta_lep` | 4.67 | ขาว |
| η Lep | `eta_lep` | 3.71 | ขาวเหลือง |
| ζ Lep | `zeta_lep` | 3.55 | ขาว |
| Arneb | `arneb` | 2.58 | ขาว |
| μ Lep | `mu_lep` | 3.29 | ฟ้าขาว |
| Arsh al Jauzah | `arsh_al_jauzah` | 3.76 | ส้ม |
| Kursi al Jabbar | `kursi_al_jabbar` | 3.59 | ขาวเหลือง |
| Nihal | `nihal` | 2.81 | ส้ม |
| ε Lep | `eps_lep` | 3.19 | ส้มแดง |
| λ Lep | `lambda_lep` | 4.29 | ฟ้าขาว |
| κ Lep | `kappa_lep` | 4.36 | ฟ้าขาว |
| ι Lep | `iota_lep` | 4.45 | ฟ้าขาว |
| ν Lep | `nu_lep` | 5.29 | ฟ้าขาว |

### 40. คันชั่ง (Libra)

`libra` ดาว 5 ดวง เส้น 5 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| θ Lib | `theta_lib` | 4.13 | ส้ม |
| Zubenelhakrabi | `zubenelhakrabi` | 3.91 | ส้ม |
| Zubeneschamali | `zubeneschamali` | 2.61 | ฟ้าขาว |
| Zubenelgenubi | `zubenelgenubi` | 2.75 | ขาว |
| Brachium | `brachium` | 3.25 | ส้มแดง |

### 41. แมวป่า (Lynx)

`lynx` ดาว 8 ดวง เส้น 7 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| α Lyn | `alpha_lyn` | 3.14 | ส้มแดง |
| 38 Lyn | `f38_lyn` | 3.82 | ขาว |
| HIP 44700 | `hip44700` | 4.56 | ส้ม |
| 10 UMa | `f10_uma` | 3.96 | ขาวเหลือง |
| Alsciaukat | `alsciaukat` | 4.25 | ส้มแดง |
| 21 Lyn | `f21_lyn` | 4.61 | ฟ้าขาว |
| 15 Lyn | `f15_lyn` | 4.35 | ส้ม |
| 2 Lyn | `f2_lyn` | 4.44 | ขาว |

### 42. พิณ (Lyra)

`lyra` ดาว 5 ดวง เส้น 5 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Vega * | `vega` | 0.03 | ฟ้าขาว |
| Nasr Alwaki | `nasr_alwaki` | 4.34 | ขาว |
| Sheliak | `sheliak` | 3.52 | ขาว |
| Sulafat | `sulafat` | 3.25 | ฟ้าขาว |
| δ² Lyr | `delta2_lyr` | 4.22 | ส้มแดง |

### 43. กล้องจุลทรรศน์ (Microscopium)

`microscopium` ดาว 3 ดวง เส้น 2 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| ε Mic | `eps_mic` | 4.71 | ขาว |
| γ Mic | `gamma_mic` | 4.67 | ส้ม |
| α Mic | `alpha_mic` | 4.89 | ส้ม |

### 44. ม้ายูนิคอร์น (Monoceros)

`monoceros` ดาว 11 ดวง เส้น 11 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| γ Mon | `gamma_mon` | 3.99 | ส้ม |
| δ Mon | `delta_mon` | 4.15 | ฟ้าขาว |
| β Mon | `beta_mon` | 3.76 | ฟ้าขาว |
| 17 Mon | `f17_mon` | 4.77 | ส้ม |
| ε Mon | `eps_mon` | 4.39 | ขาว |
| 13 Mon | `f13_mon` | 4.47 | ขาว |
| 15 Mon | `f15_mon` | 4.66 | ฟ้าขาว |
| HIP 30665 | `hip30665` | 6.60 | ขาวเหลือง |
| 28 Mon | `f28_mon` | 4.69 | ส้มแดง |
| ζ Mon | `zeta_mon` | 4.36 | ส้ม |
| α Mon | `alpha_mon` | 3.94 | ส้ม |

### 45. คนแบกงู (Ophiuchus)

`ophiuchus` ดาว 7 ดวง เส้น 7 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Rasalhague | `rasalhague` | 2.08 | ขาว |
| Cebalrai | `cebalrai` | 2.76 | ส้ม |
| Sabik | `sabik` | 2.43 | ขาว |
| κ Oph | `kappa_oph` | 3.19 | ส้ม |
| Yed Posterior | `yed_posterior` | 3.23 | ส้ม |
| Saik | `saik` | 2.54 | ขาว |
| c Oph | `c_oph` | 4.78 | ขาว |

### 46. ม้าบิน (Pegasus)

`pegasus_full` ดาว 14 ดวง เส้น 14 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Algenib * | `algenib` | 2.80 | ฟ้าขาว |
| Markab * | `markab` | 2.50 | ฟ้าขาว |
| Scheat * | `scheat` | 2.40 | ส้มแดง |
| Matar | `matar` | 2.93 | ส้ม |
| π¹ Peg | `pi1_peg` | 5.58 | ส้ม |
| Sadalbari | `sadalbari` | 3.51 | ส้ม |
| Sadalnazi | `sadalnazi` | 3.97 | ส้ม |
| ι Peg | `iota_peg` | 3.77 | ขาวเหลือง |
| κ Peg | `kappa_peg` | 4.14 | ขาวเหลือง |
| Suudalnujum | `suudalnujum` | 4.20 | ขาวเหลือง |
| Homam | `homam` | 3.41 | ฟ้าขาว |
| Biham | `biham` | 3.52 | ขาว |
| Enif | `enif` | 2.38 | ส้มแดง |
| Alpheratz * | `alpheratz` | 2.10 | ฟ้าขาว |

### 47. เพอร์ซิอัส (Perseus)

`perseus` ดาว 11 ดวง เส้น 10 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Atik | `atik` | 3.84 | ขาว |
| ζ Per | `zeta_per` | 2.84 | ขาว |
| Menkib | `menkib` | 3.98 | ขาว |
| ε Per | `eps_per` | 2.90 | ฟ้าขาว |
| δ Per | `delta_per` | 3.01 | ฟ้าขาว |
| Mirfak | `mirfak` | 1.79 | ขาวเหลือง |
| γ Per | `gamma_per` | 2.91 | ขาวเหลือง |
| Miram | `miram` | 3.77 | ส้มแดง |
| Algol | `algol` | 2.09 | ฟ้าขาว |
| Gorgonea Tertia | `gorgonea_tertia` | 3.32 | ส้มแดง |
| 16 Per | `f16_per` | 4.22 | ขาวเหลือง |

### 48. ปลาคู่ (Pisces)

`pisces` ดาว 20 ดวง เส้น 21 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| σ Psc | `sigma_psc` | 5.50 | ฟ้าขาว |
| φ Psc | `phi_psc` | 4.67 | ส้ม |
| υ Psc | `upsilon_psc` | 4.74 | ขาว |
| Alpherg | `alpherg` | 3.62 | ส้ม |
| Torcular | `torcular` | 4.26 | ส้ม |
| Alrescha | `alrescha` | 3.82 | ขาว |
| ξ Psc | `xi_psc` | 4.61 | ส้ม |
| ν Psc | `nu_psc` | 4.45 | ส้ม |
| μ Psc | `mu_psc` | 4.84 | ส้ม |
| ε Psc | `eps_psc` | 4.27 | ส้ม |
| 62 Psc | `f62_psc` | 5.92 | ส้ม |
| d Psc | `d_psc` | 5.38 | ส้ม |
| ω Psc | `omega_psc` | 4.03 | ขาวเหลือง |
| ι Psc | `iota_psc` | 4.13 | ขาวเหลือง |
| 19 Psc | `f19_psc` | 4.95 | ส้มแดง |
| λ Psc | `lambda_psc` | 4.49 | ขาว |
| κ Psc | `kappa_psc` | 4.95 | ขาว |
| γ Psc | `gamma_psc` | 3.70 | ส้ม |
| b Psc | `b_psc` | 5.05 | ส้ม |
| θ Psc | `theta_psc` | 4.27 | ส้ม |

### 49. ปลาใต้ (Piscis Austrinus)

`piscis_austrinus` ดาว 7 ดวง เส้น 6 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Fomalhaut | `fomalhaut` | 1.16 | ขาว |
| ε PsA | `eps_psa` | 4.18 | ฟ้าขาว |
| η PsA | `eta_psa` | 5.43 | ฟ้าขาว |
| θ PsA | `theta_psa` | 5.02 | ขาว |
| τ PsA | `tau_psa` | 4.94 | ขาวเหลือง |
| Fum al Hui | `fum_al_hui` | 4.29 | ขาว |
| δ PsA | `delta_psa` | 4.20 | ส้ม |

### 50. เข็มทิศ (Pyxis)

`pyxis` ดาว 3 ดวง เส้น 2 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| β Pyx | `beta_pyx` | 3.97 | ส้ม |
| α Pyx | `alpha_pyx` | 3.68 | ฟ้าขาว |
| γ Pyx | `gamma_pyx` | 4.02 | ส้ม |

### 51. ลูกศร (Sagitta)

`sagitta` ดาว 5 ดวง เส้น 4 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| β Sge | `beta_sge` | 4.39 | ส้ม |
| δ Sge | `delta_sge` | 3.68 | ส้ม |
| Sham | `sham` | 4.39 | ขาวเหลือง |
| γ Sge | `gamma_sge` | 3.51 | ส้มแดง |
| η Sge | `eta_sge` | 5.09 | ส้ม |

### 52. คนยิงธนู (Sagittarius)

`sagittarius` ดาว 21 ดวง เส้น 24 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Kaus Media | `kaus_media` | 2.72 | ส้ม |
| Kaus Borealis | `kaus_borealis` | 2.82 | ส้ม |
| Hamalwarid | `hamalwarid` | 3.10 | ส้มแดง |
| Kaus Australis | `kaus_australis` | 1.79 | ฟ้าขาว |
| Alnasl | `alnasl` | 2.98 | ส้ม |
| 3 Sgr | `f3_sgr` | 4.53 | ขาวเหลือง |
| Ascella | `ascella` | 2.60 | ขาว |
| Namalsadirah | `namalsadirah` | 3.17 | ฟ้าขาว |
| Polis | `polis` | 3.84 | ขาว |
| τ Sgr | `tau_sgr` | 3.32 | ส้ม |
| Nunki | `nunki` | 2.05 | ฟ้าขาว |
| ξ² Sgr | `xi2_sgr` | 3.52 | ส้ม |
| Manubrij | `manubrij` | 3.76 | ส้ม |
| d Sgr | `d_sgr` | 4.88 | ส้ม |
| ρ¹ Sgr | `rho1_sgr` | 3.92 | ขาว |
| h¹ Sgr | `h1_sgr` | 5.64 | ขาว |
| Terebellum | `terebellum` | 4.43 | ส้มแดง |
| θ¹ Sgr | `theta1_sgr` | 4.37 | ฟ้าขาว |
| ι Sgr | `iota_sgr` | 4.12 | ส้ม |
| Rukbat | `rukbat` | 3.96 | ฟ้าขาว |
| Arkab Posterior | `arkab_posterior` | 4.27 | ขาวเหลือง |

### 53. แมงป่อง (Scorpius)

`scorpius` ดาว 13 ดวง เส้น 12 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Shaula | `shaula` | 1.62 | ฟ้าขาว |
| Mula | `mula` | 2.39 | ฟ้าขาว |
| Girtab | `girtab` | 2.99 | ขาวเหลือง |
| Sargas | `sargas` | 1.86 | ขาวเหลือง |
| η Sco | `eta_sco` | 3.32 | ขาวเหลือง |
| ζ¹ Sco | `zeta1_sco` | 4.70 | ขาวเหลือง |
| Xamidimura | `xamidimura` | 3.00 | ฟ้าขาว |
| Larawag | `larawag` | 2.29 | ส้ม |
| Paikauhale | `paikauhale` | 2.82 | ฟ้าขาว |
| Antares | `antares` | 1.00 | ส้มแดง |
| Dschubba | `dschubba` | 2.29 | ฟ้าขาว |
| Fang | `fang` | 2.89 | ฟ้าขาว |
| Acrab | `acrab` | 2.56 | ฟ้าขาว |

### 54. ช่างแกะสลัก (Sculptor)

`sculptor` ดาว 3 ดวง เส้น 3 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| β Scl | `beta_scl` | 4.38 | ฟ้าขาว |
| α Scl | `alpha_scl` | 4.30 | ฟ้าขาว |
| γ Scl | `gamma_scl` | 4.41 | ส้ม |

### 55. โล่ (Scutum)

`scutum` ดาว 5 ดวง เส้น 5 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| β Sct | `beta_sct` | 4.22 | ส้ม |
| HIP 92202 | `hip92202` | 5.38 | ส้ม |
| HIP 92814 | `hip92814` | 5.08 | ขาว |
| γ Sct | `gamma_sct` | 4.67 | ขาว |
| α Sct | `alpha_sct` | 3.85 | ส้ม |

### 56. งู (ส่วนหัว) (Serpens Caput)

`serpens_caput` ดาว 8 ดวง เส้น 8 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Yed Prior | `yed_prior` | 2.73 | ส้มแดง |
| μ Ser | `mu_ser` | 3.54 | ฟ้าขาว |
| ε Ser | `eps_ser` | 3.71 | ขาว |
| Unukalhai | `unukalhai` | 2.63 | ส้ม |
| Nasak Yamani | `nasak_yamani` | 3.80 | ขาว |
| Nasak Shamiya | `nasak_shamiya` | 3.65 | ขาว |
| γ Ser | `gamma_ser` | 3.85 | ขาวเหลือง |
| Gudja | `gudja` | 4.09 | ส้มแดง |

### 57. งู (ส่วนหาง) (Serpens Cauda)

`serpens_cauda` ดาว 8 ดวง เส้น 7 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Alya | `alya` | 4.62 | ขาว |
| d Ser | `d_ser` | 5.20 | ขาวเหลือง |
| η Ser | `eta_ser` | 3.23 | ส้ม |
| HIP 88670 | `hip88670` | 5.84 | ขาว |
| Sinistra | `sinistra` | 3.32 | ส้ม |
| ο Ser | `omicron_ser` | 4.24 | ขาว |
| ξ Ser | `xi_ser` | 3.54 | ขาว |
| ν Ser | `nu_ser` | 4.32 | ขาว |

### 58. เครื่องวัดมุม (Sextans)

`sextans` ดาว 2 ดวง เส้น 1 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| β Sex | `beta_sex` | 5.08 | ฟ้าขาว |
| α Sex | `alpha_sex` | 4.48 | ฟ้าขาว |

### 59. สามเหลี่ยม (Triangulum)

`triangulum` ดาว 3 ดวง เส้น 3 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| γ Tri | `gamma_tri` | 4.03 | ขาว |
| Mizan | `mizan` | 3.00 | ขาว |
| Mothallah | `mothallah` | 3.42 | ขาวเหลือง |

### 60. หมีใหญ่ (Ursa Major)

`ursa_major` ดาว 18 ดวง เส้น 19 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Alkaid * | `alkaid` | 1.90 | ฟ้าขาว |
| Mizar * | `mizar` | 2.20 | ขาว |
| Alioth * | `alioth` | 1.80 | ขาว |
| Megrez * | `megrez` | 3.30 | ขาว |
| Dubhe * | `dubhe` | 1.80 | ส้ม |
| Merak * | `merak` | 2.40 | ขาว |
| Phecda * | `phecda` | 2.40 | ขาว |
| Taiyangshou | `taiyangshou` | 3.69 | ส้ม |
| ψ UMa | `psi_uma` | 3.00 | ส้ม |
| Tania Borealis | `tania_borealis` | 3.45 | ขาว |
| Tania Australis | `tania_australis` | 3.06 | ส้มแดง |
| φ UMa | `phi_uma` | 4.55 | ขาว |
| θ UMa | `theta_uma` | 3.17 | ขาวเหลือง |
| Alkaphrah | `alkaphrah` | 3.57 | ขาว |
| Talitha | `talitha` | 3.12 | ขาว |
| υ UMa | `upsilon_uma` | 3.78 | ขาว |
| Muscida | `muscida` | 3.35 | ส้ม |
| h UMa | `h_uma` | 3.65 | ขาวเหลือง |

### 61. หญิงสาว (Virgo)

`virgo` ดาว 12 ดวง เส้น 12 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| ν Vir | `nu_vir` | 4.04 | ส้มแดง |
| Zaniah | `zaniah` | 3.89 | ขาว |
| Porrima | `porrima` | 2.74 | ขาวเหลือง |
| Spica | `spica` | 0.98 | ฟ้าขาว |
| Kang | `kang` | 4.18 | ส้ม |
| Syrma | `syrma` | 4.07 | ขาวเหลือง |
| Rijl al Awwa | `rijl_al_awwa` | 3.87 | ขาวเหลือง |
| Heze | `heze` | 3.38 | ขาว |
| τ Vir | `tau_vir` | 4.23 | ขาว |
| 109 Vir | `f109_vir` | 3.73 | ฟ้าขาว |
| Minelauva | `minelauva` | 3.39 | ส้มแดง |
| Vindemiatrix | `vindemiatrix` | 2.85 | ส้ม |

### 62. หมาจิ้งจอก (Vulpecula)

`vulpecula` ดาว 2 ดวง เส้น 1 เส้น

| ดาว | key | โชติมาตร | สี |
| --- | --- | ---: | --- |
| Anser | `anser` | 4.44 | ส้มแดง |
| 15 Vul | `f15_vul` | 4.66 | ขาว |

## ดาวที่อยู่หลายกลุ่ม

| ดาว | key | กลุ่ม |
| --- | --- | --- |
| Dubhe | `dubhe` | กระบวยใหญ่, หมีใหญ่ |
| Merak | `merak` | กระบวยใหญ่, หมีใหญ่ |
| Phecda | `phecda` | กระบวยใหญ่, หมีใหญ่ |
| Megrez | `megrez` | กระบวยใหญ่, หมีใหญ่ |
| Alioth | `alioth` | กระบวยใหญ่, หมีใหญ่ |
| Mizar | `mizar` | กระบวยใหญ่, หมีใหญ่ |
| Alkaid | `alkaid` | กระบวยใหญ่, หมีใหญ่ |
| Deneb | `deneb` | หงส์, สามเหลี่ยมฤดูร้อน |
| Vega | `vega` | สามเหลี่ยมฤดูร้อน, พิณ |
| Altair | `altair` | สามเหลี่ยมฤดูร้อน, นกอินทรี |
| Elnath | `elnath` | วัว, สารถี |
| Markab | `markab` | จัตุรัสม้าบิน, ม้าบิน |
| Scheat | `scheat` | จัตุรัสม้าบิน, ม้าบิน |
| Algenib | `algenib` | จัตุรัสม้าบิน, ม้าบิน |
| Alpheratz | `alpheratz` | จัตุรัสม้าบิน, แอนดรอมิดา, ม้าบิน |

## ดาวที่ไม่อยู่ในกลุ่มไหน

วาดบนฟ้าอย่างเดียว ไม่ใช้ในเกมตามหาและลากเส้น

| ดาว | key | โชติมาตร | สี | หมวดใน catalog.lua |
| --- | --- | ---: | --- | --- |
| Alcyone | `alcyone` | 2.90 | ฟ้าขาว | ดาวลูกไก่ (ไม่อยู่ในกลุ่มที่ต้องลากเส้น วาดไว้ให้ฟ้าดูจริง) |
| Atlas | `atlas` | 3.60 | ฟ้าขาว | ดาวลูกไก่ (ไม่อยู่ในกลุ่มที่ต้องลากเส้น วาดไว้ให้ฟ้าดูจริง) |
| Electra | `electra` | 3.70 | ฟ้าขาว | ดาวลูกไก่ (ไม่อยู่ในกลุ่มที่ต้องลากเส้น วาดไว้ให้ฟ้าดูจริง) |
| Maia | `maia` | 3.90 | ฟ้าขาว | ดาวลูกไก่ (ไม่อยู่ในกลุ่มที่ต้องลากเส้น วาดไว้ให้ฟ้าดูจริง) |
| Merope | `merope` | 4.20 | ฟ้าขาว | ดาวลูกไก่ (ไม่อยู่ในกลุ่มที่ต้องลากเส้น วาดไว้ให้ฟ้าดูจริง) |
| Taygeta | `taygeta` | 4.30 | ฟ้าขาว | ดาวลูกไก่ (ไม่อยู่ในกลุ่มที่ต้องลากเส้น วาดไว้ให้ฟ้าดูจริง) |
| Pleione | `pleione` | 5.10 | ฟ้าขาว | ดาวลูกไก่ (ไม่อยู่ในกลุ่มที่ต้องลากเส้น วาดไว้ให้ฟ้าดูจริง) |

## วัตถุสำหรับเกมปรับโฟกัส

เกมปรับโฟกัสเลือกเฉพาะวัตถุที่สูงกว่า 15° ตำแหน่งดาวเคราะห์ตั้งไว้คงที่ ไม่ได้คำนวณวงโคจร

| # | ชื่อ | อังกฤษ | key | แบบภาพ | สูงสุด | กลางฟ้าเที่ยงคืน |
| ---: | --- | --- | --- | --- | ---: | --- |
| 1 | ดาวเสาร์ | Saturn | `saturn` | saturn (ดาวเคราะห์) | 54° | ก.ย. |
| 2 | ดาวพฤหัสบดี | Jupiter | `jupiter` | jupiter (ดาวเคราะห์) | 76° | ม.ค. |
| 3 | ดาวลูกไก่ (M45) | Pleiades | `pleiades` | cluster | 80° | พ.ย. |
| 4 | เนบิวลานายพราน (M42) | Orion Nebula | `orion_nebula` | nebula | 51° | ธ.ค. |
| 5 | กาแล็กซีแอนดรอเมดา (M31) | Andromeda Galaxy | `andromeda` | galaxy | 83° | ก.ย. |
| 6 | กระจุกดาวเฮอร์คิวลีส (M13) | Hercules Cluster | `hercules` | globular | 88° | พ.ค. |
| 7 | เนบิวลาวงแหวน (M57) | Ring Nebula | `ring_nebula` | ring | 89° | ก.ค. |
| 8 | อัลบิเรโอ | Albireo | `albireo_pair` | double | 84° | ก.ค. |

