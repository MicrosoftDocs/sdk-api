---
UID: NS:hrtfapoapi.HrtfDistanceDecay
title: HrtfDistanceDecay (hrtfapoapi.h)
description: Describes a distance-based decay behavior.
helpviewer_keywords: ["HrtfDistanceDecay","HrtfDistanceDecay structure [XAudio2 Audio Mixing APIs]","PHrtfDistanceDecay","PHrtfDistanceDecay structure pointer [XAudio2 Audio Mixing APIs]","hrtfapoapi/HrtfDistanceDecay","hrtfapoapi/PHrtfDistanceDecay","xaudio2.hrtfdistancedecay"]
old-location: xaudio2\hrtfdistancedecay.htm
tech.root: xaudio2
ms.assetid: B488A674-91A7-41CB-9FF5-8270C6E941D2
ms.date: 12/05/2018
ms.keywords: HrtfDistanceDecay, HrtfDistanceDecay structure [XAudio2 Audio Mixing APIs], PHrtfDistanceDecay, PHrtfDistanceDecay structure pointer [XAudio2 Audio Mixing APIs], hrtfapoapi/HrtfDistanceDecay, hrtfapoapi/PHrtfDistanceDecay, xaudio2.hrtfdistancedecay
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
targetos: Windows
req.typenames: HrtfDistanceDecay
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HrtfDistanceDecay
 - hrtfapoapi/HrtfDistanceDecay
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - HrtfApoApi.h
api_name:
 - HrtfDistanceDecay
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

<a href="/windows/desktop/api/hrtfapoapi/ns-hrtfapoapi-hrtfapoinit">HrtfApoInit</a>



<a href="/windows/desktop/api/hrtfapoapi/ne-hrtfapoapi-hrtfdistancedecaytype">HrtfDistanceDecayType</a>



<a href="/windows/desktop/xaudio2/structures">Structures</a>