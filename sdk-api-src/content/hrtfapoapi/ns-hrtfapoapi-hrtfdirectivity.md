---
UID: NS:hrtfapoapi.HrtfDirectivity
title: HrtfDirectivity (hrtfapoapi.h)
description: Base directivity pattern descriptor. Describes the type of directivity applied to a sound.
helpviewer_keywords: ["HrtfDirectivity","HrtfDirectivity structure [XAudio2 Audio Mixing APIs]","PHrtfDirectivity","PHrtfDirectivity structure pointer [XAudio2 Audio Mixing APIs]","hrtfapoapi/HrtfDirectivity","hrtfapoapi/PHrtfDirectivity","xaudio2.hrtfdirectivity"]
old-location: xaudio2\hrtfdirectivity.htm
tech.root: xaudio2
ms.assetid: 830DB9FC-B2D0-46E5-B0C1-0BBC94D37050
ms.date: 12/05/2018
ms.keywords: HrtfDirectivity, HrtfDirectivity structure [XAudio2 Audio Mixing APIs], PHrtfDirectivity, PHrtfDirectivity structure pointer [XAudio2 Audio Mixing APIs], hrtfapoapi/HrtfDirectivity, hrtfapoapi/PHrtfDirectivity, xaudio2.hrtfdirectivity
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
req.typenames: HrtfDirectivity
req.redist: 
ms.custom: 19H1
f1_keywords:
 - HrtfDirectivity
 - hrtfapoapi/HrtfDirectivity
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
 - HrtfDirectivity
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

<a href="/windows/desktop/api/hrtfapoapi/ne-hrtfapoapi-hrtfdirectivitytype">HrtfDirectivityType</a>



<a href="/windows/desktop/xaudio2/structures">Structures</a>