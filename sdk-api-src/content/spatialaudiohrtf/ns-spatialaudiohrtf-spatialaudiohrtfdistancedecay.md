---
UID: NS:spatialaudiohrtf.SpatialAudioHrtfDistanceDecay
title: SpatialAudioHrtfDistanceDecay
author: windows-sdk-content
description: Represents the decay model that is applied over distance from the position of an ISpatialAudioObjectForHrtf to the position of the listener.
old-location: coreaudio\spatialaudiohrtfdistancedecay.htm
old-project: CoreAudio
ms.assetid: 2EBAE322-2A5F-4610-B64F-F1B8CE2DFD2D
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: SpatialAudioHrtfDistanceDecay, SpatialAudioHrtfDistanceDecay union [Core Audio], coreaudio.spatialaudiohrtfdistancedecay, spatialaudiohrtf/SpatialAudioHrtfDistanceDecay
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: spatialaudiohrtf.h
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
req.typenames: SpatialAudioHrtfDistanceDecay
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - spatialaudiohrtf.h
api_name:
 - SpatialAudioHrtfDistanceDecay
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# SpatialAudioHrtfDistanceDecay structure


## -description


Represents the decay model that is applied over distance from the position of an <a href="https://msdn.microsoft.com/E69F1D09-B937-4BCC-A040-18EF8A838289">ISpatialAudioObjectForHrtf</a> to the position of the listener. 


## -struct-fields




### -field Type

The type of decay, natural or custom. The default value for this field is  <b>SpatialAudioHrtfDistanceDecay_NaturalDecay</b>.


### -field MaxGain

 


### -field MinGain

 


### -field UnityGainDistance

 


### -field CutoffDistance

 




#### - float

The maximum gain limit applied at any distance. Applies to both natural and custom decay. This value is specified in dB, with a range from -96 to 12 inclusive. The default value is 12 dB. 

The minimum gain limit applied at any distance. Applies to both natural and custom decay. This value is specified in dB, with a range from -96 to 12 inclusive. The default value is -96 dB.

The distance at which the gain is 0dB. Applies to natural decay only. This value is specified in meters, with a range from 0.05 to infinity (<b>FLT_MAX</b>). The default value is 1 meter. 

The distance at which  the output is silent. Applies to natural decay only. This value is specified in meters, with a range from zero (non-inclusive) to infinity (<b>FLT_MAX</b>). The default value is <b>INFINITY</b>.

