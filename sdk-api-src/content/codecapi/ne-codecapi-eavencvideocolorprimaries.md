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

# eAVEncVideoColorPrimaries enumeration


## -description



Specifies the color primaries of the video. This enumeration is used with the <a href="https://msdn.microsoft.com/2134fa6e-9e8e-4a83-9593-b5ae8c6d3e42">AVEncVideoInputColorPrimaries</a> and <a href="https://msdn.microsoft.com/f0369dee-12e4-4403-a0c4-6d840ad2552e">AVEncVideoOutputColorPrimaries</a> properties.




## -enum-fields




### -field eAVEncVideoColorPrimaries_SameAsSource

Use the same primaries as the input video. This flag applies to the <b>AVEncVideoOutputColorPrimaries</b> property only.


### -field eAVEncVideoColorPrimaries_Reserved

Reserved. Do not use.


### -field eAVEncVideoColorPrimaries_BT709

ITU-R BT.709 (including sRGB and scRGB).


### -field eAVEncVideoColorPrimaries_BT470_2_SysM

ITU-R.BT.470-4 System M (NTSC).


### -field eAVEncVideoColorPrimaries_BT470_2_SysBG

ITU-R.BT.470-4 System B,G (NTSC).


### -field eAVEncVideoColorPrimaries_SMPTE170M

SMPTE 170M.


### -field eAVEncVideoColorPrimaries_SMPTE240M

SMPTE 240M.


### -field eAVEncVideoColorPrimaries_EBU3231

EBU 3213.


### -field eAVEncVideoColorPrimaries_SMPTE_C

SPMTE C (NTSC).


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

