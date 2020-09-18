---
UID: NS:x3daudio.X3DAUDIO_DISTANCE_CURVE
title: X3DAUDIO_DISTANCE_CURVE (x3daudio.h)
description: Defines an explicit piecewise curve made up of linear segments, directly defining DSP behavior with respect to normalized distance.
helpviewer_keywords: ["*LPX3DAUDIO_DISTANCE_CURVE","LPX3DAUDIO_DISTANCE_CURVE","LPX3DAUDIO_DISTANCE_CURVE structure pointer [XAudio2 Audio Mixing APIs]","X3DAUDIO_DISTANCE_CURVE","X3DAUDIO_DISTANCE_CURVE structure [XAudio2 Audio Mixing APIs]","x3daudio/LPX3DAUDIO_DISTANCE_CURVE","x3daudio/X3DAUDIO_DISTANCE_CURVE","xaudio2.x3daudio_distance_curve"]
old-location: xaudio2\x3daudio_distance_curve.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.x3daudio.X3DAUDIO_DISTANCE_CURVE
ms.date: 12/05/2018
ms.keywords: '*LPX3DAUDIO_DISTANCE_CURVE, LPX3DAUDIO_DISTANCE_CURVE, LPX3DAUDIO_DISTANCE_CURVE structure pointer [XAudio2 Audio Mixing APIs], X3DAUDIO_DISTANCE_CURVE, X3DAUDIO_DISTANCE_CURVE structure [XAudio2 Audio Mixing APIs], x3daudio/LPX3DAUDIO_DISTANCE_CURVE, x3daudio/X3DAUDIO_DISTANCE_CURVE, xaudio2.x3daudio_distance_curve'
req.header: x3daudio.h
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
req.typenames: X3DAUDIO_DISTANCE_CURVE, *LPX3DAUDIO_DISTANCE_CURVE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X3DAUDIO_DISTANCE_CURVE
 - x3daudio/X3DAUDIO_DISTANCE_CURVE
 - LPX3DAUDIO_DISTANCE_CURVE
 - x3daudio/LPX3DAUDIO_DISTANCE_CURVE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - x3daudio.h
api_name:
 - X3DAUDIO_DISTANCE_CURVE
---

# X3DAUDIO_DISTANCE_CURVE structure


## -description

Defines an explicit piecewise curve made up of linear segments, directly defining DSP behavior with respect to normalized distance.

## -struct-fields

### -field pPoints

<a href="/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve_point">X3DAUDIO_DISTANCE_CURVE_POINT</a> array. The array must have no duplicates and be sorted in ascending order with respect to distance.

### -field PointCount

Number of distance curve points. There must be two or more points since all curves must have at least two endpoints defining values at 0.0f and 1.0f normalized distance, respectively.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>