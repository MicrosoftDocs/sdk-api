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
 

 

