---
UID: NS:hrtfapoapi.HrtfDirectivityCardioid
title: HrtfDirectivityCardioid
author: windows-sdk-content
description: Describes a cardioid directivity pattern.
old-location: xaudio2\hrtfdirectivitycardioid.htm
tech.root: xaudio2
ms.assetid: 0705BB4C-01FE-434A-889B-F0D24D06DEF3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: HrtfDirectivityCardioid, HrtfDirectivityCardioid structure [XAudio2 Audio Mixing APIs], PHrtfDirectivityCardioid, PHrtfDirectivityCardioid structure pointer [XAudio2 Audio Mixing APIs], hrtfapoapi/HrtfDirectivityCardioid, hrtfapoapi/PHrtfDirectivityCardioid, xaudio2.hrtfdirectivitycardioid
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - HrtfApoApi.h
api_name:
 - HrtfDirectivityCardioid
product: Windows
targetos: Windows
req.typenames: HrtfDirectivityCardioid
req.redist: 
---

# HrtfDirectivityCardioid structure


## -description


Describes a cardioid directivity pattern. 


## -struct-fields




### -field directivity

Descriptor for the cardioid pattern. The type parameter must be set to HrtfDirectivityType.Cardioid.


### -field order

Controls the shape of the cardioid. The higher order the shape, the narrower it is. Must be greater than 0 and less than or equal to 32.


## -see-also




<a href="https://msdn.microsoft.com/830DB9FC-B2D0-46E5-B0C1-0BBC94D37050">HrtfDirectivity</a>



<a href="https://msdn.microsoft.com/88679E17-285A-41C1-87A5-C37AF66F327F">HrtfDirectivityCone</a>



<a href="https://msdn.microsoft.com/3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c">Structures</a>
 

 

