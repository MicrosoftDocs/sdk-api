---
UID: NS:hrtfapoapi.HrtfDirectivity
title: HrtfDirectivity
author: windows-sdk-content
description: Base directivity pattern descriptor. Describes the type of directivity applied to a sound.
old-location: xaudio2\hrtfdirectivity.htm
old-project: xaudio2
ms.assetid: 830DB9FC-B2D0-46E5-B0C1-0BBC94D37050
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: HrtfDirectivity, HrtfDirectivity structure [XAudio2 Audio Mixing APIs], PHrtfDirectivity, PHrtfDirectivity structure pointer [XAudio2 Audio Mixing APIs], hrtfapoapi/HrtfDirectivity, hrtfapoapi/PHrtfDirectivity, xaudio2.hrtfdirectivity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: hrtfapoapi.h
req.include-header: 
req.target-type: Windows
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
req.typenames: HrtfDirectivity
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	HrtfApoApi.h
api_name:
-	HrtfDirectivity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# HrtfDirectivity structure


## -description


Base directivity pattern descriptor. Describes the type of directivity applied to a sound.


## -struct-fields




### -field type

Indicates the type of directivity.


### -field scaling

A normalized value between zero and one. Specifies the amount of linear interpolation between omnidirectional sound and the full directivity pattern, where 0 is fully omnidirectional and 1 is fully directional.


## -remarks



The scaling parameter is used to interpolate between directivity behavior and omnidirectional; it determines how much attenuation is applied to the source outside of the directivity pattern and controls how directional the source is.

For fully directional sources, while direct path signal outside the directivity pattern will be fully attenuated, any environmental reflections will still be audible.




## -see-also




<a href="https://msdn.microsoft.com/7E094590-993D-4DA2-9955-A07E23B2604E">HrtfDirectivityType</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

