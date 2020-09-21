---
UID: NS:hrtfapoapi.HrtfDirectivityCone
title: HrtfDirectivityCone (hrtfapoapi.h)
description: Describes a cone directivity.
helpviewer_keywords: ["HrtfDirectivityCone","HrtfDirectivityCone structure [XAudio2 Audio Mixing APIs]","PHrtfDirectivityCone","PHrtfDirectivityCone structure pointer [XAudio2 Audio Mixing APIs]","hrtfapoapi/HrtfDirectivityCone","hrtfapoapi/PHrtfDirectivityCone","xaudio2.hrtfdirectivitycone"]
old-location: xaudio2\hrtfdirectivitycone.htm
tech.root: xaudio2
ms.assetid: 88679E17-285A-41C1-87A5-C37AF66F327F
ms.date: 12/05/2018
ms.keywords: HrtfDirectivityCone, HrtfDirectivityCone structure [XAudio2 Audio Mixing APIs], PHrtfDirectivityCone, PHrtfDirectivityCone structure pointer [XAudio2 Audio Mixing APIs], hrtfapoapi/HrtfDirectivityCone, hrtfapoapi/PHrtfDirectivityCone, xaudio2.hrtfdirectivitycone
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
req.typenames: HrtfDirectivityCone
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HrtfDirectivityCone
 - hrtfapoapi/HrtfDirectivityCone
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
 - HrtfDirectivityCone
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

<a href="/windows/desktop/api/hrtfapoapi/ns-hrtfapoapi-hrtfdirectivity">HrtfDirectivity</a>



<a href="/windows/desktop/api/hrtfapoapi/ns-hrtfapoapi-hrtfdirectivitycardioid">HrtfDirectivityCardioid</a>



<a href="/windows/desktop/xaudio2/structures">Structures</a>