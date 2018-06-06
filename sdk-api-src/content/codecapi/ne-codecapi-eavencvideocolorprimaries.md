---
UID: NE:codecapi.eAVEncVideoColorPrimaries
title: eAVEncVideoColorPrimaries
author: windows-sdk-content
description: Specifies the color primaries of the video. This enumeration is used with the AVEncVideoInputColorPrimaries and AVEncVideoOutputColorPrimaries properties.
old-location: dshow\eavencvideocolorprimaries.htm
old-project: DirectShow
ms.assetid: dd86a0e2-79ba-4d40-9a2f-a7dd6c6ab36d
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: codecapi/eAVEncVideoColorPrimaries, codecapi/eAVEncVideoColorPrimaries_BT470_2_SysBG, codecapi/eAVEncVideoColorPrimaries_BT470_2_SysM, codecapi/eAVEncVideoColorPrimaries_BT709, codecapi/eAVEncVideoColorPrimaries_EBU3231, codecapi/eAVEncVideoColorPrimaries_Reserved, codecapi/eAVEncVideoColorPrimaries_SMPTE170M, codecapi/eAVEncVideoColorPrimaries_SMPTE240M, codecapi/eAVEncVideoColorPrimaries_SMPTE_C, codecapi/eAVEncVideoColorPrimaries_SameAsSource, dshow.eavencvideocolorprimaries, eAVEncVideoColorPrimaries, eAVEncVideoColorPrimaries enumeration [DirectShow], eAVEncVideoColorPrimariesEnumeration, eAVEncVideoColorPrimaries_BT470_2_SysBG, eAVEncVideoColorPrimaries_BT470_2_SysM, eAVEncVideoColorPrimaries_BT709, eAVEncVideoColorPrimaries_EBU3231, eAVEncVideoColorPrimaries_Reserved, eAVEncVideoColorPrimaries_SMPTE170M, eAVEncVideoColorPrimaries_SMPTE240M, eAVEncVideoColorPrimaries_SMPTE_C, eAVEncVideoColorPrimaries_SameAsSource
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVEncVideoColorPrimaries
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

