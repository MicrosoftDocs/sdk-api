---
UID: NS:hrtfapoapi.HrtfDistanceDecay
title: HrtfDistanceDecay
author: windows-sdk-content
description: Describes a distance-based decay behavior.
old-location: xaudio2\hrtfdistancedecay.htm
old-project: xaudio2
ms.assetid: B488A674-91A7-41CB-9FF5-8270C6E941D2
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: HrtfDistanceDecay, HrtfDistanceDecay structure [XAudio2 Audio Mixing APIs], PHrtfDistanceDecay, PHrtfDistanceDecay structure pointer [XAudio2 Audio Mixing APIs], hrtfapoapi/HrtfDistanceDecay, hrtfapoapi/PHrtfDistanceDecay, xaudio2.hrtfdistancedecay
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
req.typenames: HrtfDistanceDecay
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	HrtfApoApi.h
api_name:
-	HrtfDistanceDecay
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# HrtfDistanceDecay structure


## -description


Describes a distance-based decay behavior.


## -struct-fields




### -field type

The type of decay behavior, natural or custom.


### -field maxGain

The maximum gain limit applied at any distance. Applies to both natural and custom decay. This value is specified in dB, with a range from -96 to 12 inclusive. The default value is 12 dB.


### -field minGain

The minimum gain limit applied at any distance. Applies to both natural and custom decay. This value is specified in dB, with a range from -96 to 12 inclusive. The default value is -96 dB.


### -field unityGainDistance

The distance at which the gain is 0dB. Applies to natural decay only. This value is specified in meters, with a range from 0.05 to infinity (FLT_MAX). The default value is 1 meter.


### -field cutoffDistance

The distance at which output is silent. Applies to natural decay only. This value is specified in meters, with a range from zero (non-inclusive) to infinity (FLT_MAX). The default value is infinity.


## -see-also




<a href="https://msdn.microsoft.com/686A2203-A991-427F-9D41-F3C679070127">HrtfApoInit</a>



<a href="https://msdn.microsoft.com/72421F09-6DB6-4195-AE44-0D3AD17F50B3">HrtfDistanceDecayType</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

