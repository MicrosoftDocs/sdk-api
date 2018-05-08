---
UID: NE:codecapi.eAVDecDDOperationalMode
title: eAVDecDDOperationalMode
author: windows-driver-content
description: Specifies the compression control mode for a Dolby AC-3 audio stream. This enumeration is used with the AVDecDDOperationalMode property.
old-location: dshow\eavdecddoperationalmode.htm
old-project: DirectShow
ms.assetid: 00d3f086-eaba-4bd2-ba77-401101e92570
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: codecapi/eAVDecDDOperationalMode, codecapi/eAVDecDDOperationalMode_CUSTOM0, codecapi/eAVDecDDOperationalMode_CUSTOM1, codecapi/eAVDecDDOperationalMode_LINE, codecapi/eAVDecDDOperationalMode_NONE, codecapi/eAVDecDDOperationalMode_PORTABLE11, codecapi/eAVDecDDOperationalMode_PORTABLE14, codecapi/eAVDecDDOperationalMode_PORTABLE8, codecapi/eAVDecDDOperationalMode_RF, dshow.eavdecddoperationalmode, eAVDecDDOperationalMode, eAVDecDDOperationalMode enumeration [DirectShow], eAVDecDDOperationalModeEnumeration, eAVDecDDOperationalMode_CUSTOM0, eAVDecDDOperationalMode_CUSTOM1, eAVDecDDOperationalMode_LINE, eAVDecDDOperationalMode_NONE, eAVDecDDOperationalMode_PORTABLE11, eAVDecDDOperationalMode_PORTABLE14, eAVDecDDOperationalMode_PORTABLE8, eAVDecDDOperationalMode_RF
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	codecapi.h
api_name:
-	eAVDecDDOperationalMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# eAVDecDDOperationalMode enumeration


## -description



Specifies the compression control mode for a Dolby AC-3 audio stream. This enumeration is used with the <a href="https://msdn.microsoft.com/c235f28e-94b2-44ec-9915-c4161b40a71c">AVDecDDOperationalMode</a> property.




## -enum-fields




### -field eAVDecDDOperationalMode_NONE

No dynamic range control or dialogue normalization (dialnorm). This mode should be used only for signal tests.


### -field eAVDecDDOperationalMode_LINE

Line mode. Dialnorm is enabled with a reference level of -31 decibels full scale (dBFS). Dynamic range control is applied, and high-level/low-level scaling is enabled. To set the high-level scaling factor, set the <a href="https://msdn.microsoft.com/8771a5f9-878b-43fd-8eaa-0bfc276194aa">AVDecDDDynamicRangeScaleHigh</a> property. To set the low-level scaling factor, set the <a href="https://msdn.microsoft.com/d723c825-f2f1-4ba0-a667-8285009764fd">AVDecDDDynamicRangeScaleLow</a> property.


### -field eAVDecDDOperationalMode_RF

RF mode. Dialnorm is enabled with a reference level of -20 dBFS. Dynamic range control is applied. High-level/low-level scaling is disabled; instead, the maximum dynamic range reduction is applied.


### -field eAVDecDDOperationalMode_CUSTOM0

Custom mode 0 (analog dialnorm).


### -field eAVDecDDOperationalMode_CUSTOM1

Custom mode 1 (digital dialnorm).


### -field eAVDecDDOperationalMode_PORTABLE8

Dialnorm enabled, dialogue at -8dBFS. Dynamic range and compression used. High-level/low-level scaling is not allowed (always fully compressed).


### -field eAVDecDDOperationalMode_PORTABLE11

Dialnorm enabled, dialogue at -11dBFS. Dynamic range and compression used. High-level/low-level scaling is not allowed (always fully compressed).


### -field eAVDecDDOperationalMode_PORTABLE14

Dialnorm enabled, dialogue at -14dBFS. Dynamic range and compression used. High-level/low-level scaling is not allowed (always fully compressed).


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

