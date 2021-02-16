---
UID: NS:x3daudio.X3DAUDIO_CONE
title: X3DAUDIO_CONE (x3daudio.h)
description: Specifies directionality for a single-channel non-LFE emitter by scaling DSP behavior with respect to the emitter's orientation.
helpviewer_keywords: ["*LPX3DAUDIO_CONE","LPX3DAUDIO_CONE","LPX3DAUDIO_CONE structure pointer [XAudio2 Audio Mixing APIs]","X3DAUDIO_CONE","X3DAUDIO_CONE structure [XAudio2 Audio Mixing APIs]","x3daudio/LPX3DAUDIO_CONE","x3daudio/X3DAUDIO_CONE","xaudio2.x3daudio_cone"]
old-location: xaudio2\x3daudio_cone.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.x3daudio.X3DAUDIO_CONE
ms.date: 12/05/2018
ms.keywords: '*LPX3DAUDIO_CONE, LPX3DAUDIO_CONE, LPX3DAUDIO_CONE structure pointer [XAudio2 Audio Mixing APIs], X3DAUDIO_CONE, X3DAUDIO_CONE structure [XAudio2 Audio Mixing APIs], x3daudio/LPX3DAUDIO_CONE, x3daudio/X3DAUDIO_CONE, xaudio2.x3daudio_cone'
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
req.typenames: X3DAUDIO_CONE, *LPX3DAUDIO_CONE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X3DAUDIO_CONE
 - x3daudio/X3DAUDIO_CONE
 - LPX3DAUDIO_CONE
 - x3daudio/LPX3DAUDIO_CONE
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
 - X3DAUDIO_CONE
---

# X3DAUDIO_CONE structure


## -description

Specifies directionality for a single-channel non-LFE emitter by scaling DSP behavior with respect to the emitter's orientation.

## -struct-fields

### -field InnerAngle

Inner cone angle in radians. This value must be within 0.0f to X3DAUDIO_2PI.

### -field OuterAngle

Outer cone angle in radians. This value must be within <i>InnerAngle</i> to X3DAUDIO_2PI.

### -field InnerVolume

Volume scaler on/within inner cone. This value must be within 0.0f to 2.0f.

### -field OuterVolume

Volume scaler on/beyond outer cone. This value must be within 0.0f to 2.0f.

### -field InnerLPF

LPF direct-path or reverb-path coefficient scaler on/within inner cone. This value is only used for LPF calculations and must be within 0.0f to 1.0f.

### -field OuterLPF

LPF direct-path or reverb-path coefficient scaler on or beyond outer cone. This value is only used for LPF calculations and must be within 0.0f to 1.0f.

### -field InnerReverb

Reverb send level scaler on or within inner cone. This must be within 0.0f to 2.0f.

### -field OuterReverb

Reverb send level scaler on/beyond outer cone. This must be within 0.0f to 2.0f.

## -remarks

For a detailed explanation of sound cones see <a href="/windows/desktop/xaudio2/sound-cones">Sound Cones</a>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>