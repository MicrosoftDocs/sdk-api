---
UID: NS:x3daudio.X3DAUDIO_DISTANCE_CURVE_POINT
title: X3DAUDIO_DISTANCE_CURVE_POINT (x3daudio.h)
description: Defines a DSP setting at a given normalized distance.
helpviewer_keywords: ["*LPX3DAUDIO_DISTANCE_CURVE_POINT","LPX3DAUDIO_DISTANCE_CURVE_POINT","LPX3DAUDIO_DISTANCE_CURVE_POINT structure pointer [XAudio2 Audio Mixing APIs]","X3DAUDIO_DISTANCE_CURVE_POINT","X3DAUDIO_DISTANCE_CURVE_POINT structure [XAudio2 Audio Mixing APIs]","x3daudio/LPX3DAUDIO_DISTANCE_CURVE_POINT","x3daudio/X3DAUDIO_DISTANCE_CURVE_POINT","xaudio2.x3daudio_distance_curve_point"]
old-location: xaudio2\x3daudio_distance_curve_point.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.x3daudio.X3DAUDIO_DISTANCE_CURVE_POINT
ms.date: 12/05/2018
ms.keywords: '*LPX3DAUDIO_DISTANCE_CURVE_POINT, LPX3DAUDIO_DISTANCE_CURVE_POINT, LPX3DAUDIO_DISTANCE_CURVE_POINT structure pointer [XAudio2 Audio Mixing APIs], X3DAUDIO_DISTANCE_CURVE_POINT, X3DAUDIO_DISTANCE_CURVE_POINT structure [XAudio2 Audio Mixing APIs], x3daudio/LPX3DAUDIO_DISTANCE_CURVE_POINT, x3daudio/X3DAUDIO_DISTANCE_CURVE_POINT, xaudio2.x3daudio_distance_curve_point'
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
req.typenames: X3DAUDIO_DISTANCE_CURVE_POINT, *LPX3DAUDIO_DISTANCE_CURVE_POINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X3DAUDIO_DISTANCE_CURVE_POINT
 - x3daudio/X3DAUDIO_DISTANCE_CURVE_POINT
 - LPX3DAUDIO_DISTANCE_CURVE_POINT
 - x3daudio/LPX3DAUDIO_DISTANCE_CURVE_POINT
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
 - X3DAUDIO_DISTANCE_CURVE_POINT
---

# X3DAUDIO_DISTANCE_CURVE_POINT structure


## -description

Defines a DSP setting at a given normalized distance.

## -struct-fields

### -field Distance

Normalized distance. This must be within 0.0f to 1.0f.

### -field DSPSetting

DSP control setting.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>