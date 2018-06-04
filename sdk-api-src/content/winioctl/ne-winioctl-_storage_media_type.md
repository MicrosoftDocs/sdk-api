---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _STORAGE_MEDIA_TYPE enumeration


## -description


Specifies various types of storage media. Parameters and members of type 
    <b>STORAGE_MEDIA_TYPE</b> also accept values from the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff562216">MEDIA_TYPE</a> enumeration type.


## -enum-fields




### -field DDS_4mm

One of the following tape types: DAT, DDS1, DDS2, and so on.


### -field MiniQic

MiniQIC tape.


### -field Travan

Travan tape (TR-1, TR-2, TR-3, and so on).


### -field QIC

QIC tape.


### -field MP_8mm

An 8mm Exabyte metal particle tape.


### -field AME_8mm

An 8mm Exabyte advanced metal evaporative tape.


### -field AIT1_8mm

An 8mm Sony AIT1 tape.


### -field DLT

DLT compact tape (IIIxt or IV).


### -field NCTP

Philips NCTP tape.


### -field IBM_3480

IBM 3480 tape.


### -field IBM_3490E

IBM 3490E tape.


### -field IBM_Magstar_3590

IBM Magstar 3590 tape.


### -field IBM_Magstar_MP

IBM Magstar MP tape.


### -field STK_DATA_D3

STK data D3 tape.


### -field SONY_DTF

Sony DTF tape.


### -field DV_6mm

A 6mm digital videotape.


### -field DMI

Exabyte DMI tape (or compatible).


### -field SONY_D2

Sony D2S or D2L tape.


### -field CLEANER_CARTRIDGE

Cleaner (all drive types that support cleaners).


### -field CD_ROM

CD.


### -field CD_R

CD (write once).


### -field CD_RW

CD (rewriteable).


### -field DVD_ROM

DVD.


### -field DVD_R

DVD (write once).


### -field DVD_RW

DVD (rewriteable).


### -field MO_3_RW

Magneto-optical 3.5" (rewriteable).


### -field MO_5_WO

Magneto-optical 5.25" (write once).


### -field MO_5_RW

Magneto-optical 5.25" (rewriteable; not LIMDOW).


### -field MO_5_LIMDOW

Magneto-optical 5.25" (rewriteable; LIMDOW).


### -field PC_5_WO

Phase change 5.25" (write once)


### -field PC_5_RW

Phase change 5.25" (rewriteable)


### -field PD_5_RW

Phase change dual (rewriteable)


### -field ABL_5_WO

Ablative 5.25" (write once).


### -field PINNACLE_APEX_5_RW

Pinnacle Apex 4.6GB (rewriteable)


### -field SONY_12_WO

Sony 12" (write once).


### -field PHILIPS_12_WO

Philips/LMS 12" (write once).


### -field HITACHI_12_WO

Hitachi 12" (write once)


### -field CYGNET_12_WO

Cygnet/ATG 12" (write once)


### -field KODAK_14_WO

Kodak 14" (write once)


### -field MO_NFR_525

MO near field recording (Terastor)


### -field NIKON_12_RW

Nikon 12" (rewriteable).


### -field IOMEGA_ZIP

Iomega Zip.


### -field IOMEGA_JAZ

Iomega Jaz.


### -field SYQUEST_EZ135

Syquest EZ135.


### -field SYQUEST_EZFLYER

Syquest EzFlyer.


### -field SYQUEST_SYJET

Syquest SyJet.


### -field AVATAR_F2

Avatar 2.5" floppy.


### -field MP2_8mm

An 8mm Hitachi tape.


### -field DST_S

Ampex DST small tape.


### -field DST_M

Ampex DST medium tape.


### -field DST_L

Ampex DST large tape.


### -field VXATape_1

Ecrix 8mm tape.


### -field VXATape_2

Ecrix 8mm tape.


### -field STK_EAGLE


### -field LTO_Ultrium

LTO Ultrium (IBM, HP, Seagate).


### -field LTO_Accelis

LTO Accelis (IBM, HP, Seagate).


### -field DVD_RAM

DVD-RAM.


### -field AIT_8mm

AIT tape (AIT2 or higher).


### -field ADR_1

OnStream ADR1.


### -field ADR_2

OnStream ADR2.


### -field STK_9940

STK 9940.


### -field SAIT

SAIT tape.

<b>Windows Server 2003:  </b>This is not supported before Windows Server 2003 with SP1.


### -field VXATape

Exabyte VXA tape.

<b>Windows Server 2008:  </b>This is not supported before Windows Server 2008.


#### - STK_9840

STK 9840.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552529">DEVICE_MEDIA_INFO</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff562216">MEDIA_TYPE</a>



<a href="https://msdn.microsoft.com/38020a77-0340-4096-a2a8-d16eec5857e6">NTMS_MEDIATYPEINFORMATION</a>
 

 

