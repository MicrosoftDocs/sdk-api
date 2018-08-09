---
UID: NS:hrtfapoapi.HrtfDirectivityCone
title: HrtfDirectivityCone
author: windows-sdk-content
description: Describes a cone directivity.
old-location: xaudio2\hrtfdirectivitycone.htm
old-project: xaudio2
ms.assetid: 88679E17-285A-41C1-87A5-C37AF66F327F
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: HrtfDirectivityCone, HrtfDirectivityCone structure [XAudio2 Audio Mixing APIs], PHrtfDirectivityCone, PHrtfDirectivityCone structure pointer [XAudio2 Audio Mixing APIs], hrtfapoapi/HrtfDirectivityCone, hrtfapoapi/PHrtfDirectivityCone, xaudio2.hrtfdirectivitycone
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
tech.root: 
req.typenames: HrtfDirectivityCone
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - HrtfApoApi.h
api_name:
 - HrtfDirectivityCone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# HrtfDirectivityCone structure


## -description


Describes a cone directivity.


## -struct-fields




### -field directivity

Descriptor for the cone pattern. The type parameter must be set to HrtfDirectivityType.Cone. 


### -field innerAngle

Angle, in radians, that defines the inner cone. Must be between 0 and 2 * pi.


### -field outerAngle

Angle, in radians, that defines the outer cone. Must be between 0 and 2 * pi.


## -remarks



Attenuation is 0 inside the inner cone.   Attenuation is linearly interpolated between the inner cone, which is defined by <i>innerAngle</i>, and the outer cone, which is defined by <i>outerAngle.</i>




## -see-also




<a href="https://msdn.microsoft.com/830DB9FC-B2D0-46E5-B0C1-0BBC94D37050">HrtfDirectivity</a>



<a href="https://msdn.microsoft.com/0705BB4C-01FE-434A-889B-F0D24D06DEF3">HrtfDirectivityCardioid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

