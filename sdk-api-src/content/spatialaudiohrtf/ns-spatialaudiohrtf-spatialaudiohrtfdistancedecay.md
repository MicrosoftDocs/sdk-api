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

