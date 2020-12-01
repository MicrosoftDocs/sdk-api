---
UID: NF:xaudio2fx.ReverbConvertI3DL2ToNative
title: ReverbConvertI3DL2ToNative function (xaudio2fx.h)
description: Inline function that converts I3DL2 (Interactive 3D Audio Rendering Guidelines Level 2.0) parameters to native XAudio2 parameters.
helpviewer_keywords: ["ReverbConvertI3DL2ToNative","ReverbConvertI3DL2ToNative function [XAudio2 Audio Mixing APIs]","xaudio2.reverbconverti3dl2tonative","xaudio2fx/ReverbConvertI3DL2ToNative"]
old-location: xaudio2\reverbconverti3dl2tonative.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xaudio2.ReverbConvertI3DL2ToNative(const XAUDIO2FX_REVERB_I3DL2_PARAMETERS,XAUDIO2FX_REVERB_PARAMETERS@)
ms.date: 12/05/2018
ms.keywords: ReverbConvertI3DL2ToNative, ReverbConvertI3DL2ToNative function [XAudio2 Audio Mixing APIs], xaudio2.reverbconverti3dl2tonative, xaudio2fx/ReverbConvertI3DL2ToNative
req.header: xaudio2fx.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ReverbConvertI3DL2ToNative
 - xaudio2fx/ReverbConvertI3DL2ToNative
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xaudio2fx.h
api_name:
 - ReverbConvertI3DL2ToNative
---

# ReverbConvertI3DL2ToNative function


## -description

Inline function that converts I3DL2 (Interactive 3D Audio Rendering Guidelines Level 2.0) parameters to native XAudio2 parameters.

## -parameters

### -param pI3DL2 [in]

Pointer to a <a href="/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_i3dl2_parameters">XAUDIO2FX_REVERB_I3DL2_PARAMETERS</a> structure containing the I3DL2 parameters to convert. There are many preset values defined for the <b>XAUDIO2FX_REVERB_I3DL2_PARAMETERS</b> structure; for more information, see <a href="/windows/desktop/xaudio2/xaudio2fx-i3dl2-preset">XAUDIO2FX_I3DL2_PRESET</a>.

### -param pNative [in, out]

Pointer to a <a href="/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters">XAUDIO2FX_REVERB_PARAMETERS</a> structure that will receive the native parameters that are equivalent to the I3DL2 parameters.

### -param sevenDotOneReverb

A boolean value indicating whether 7.1 reverb is enabled.

<div class="alert"><b>Note</b>  This parameter is supported beginning with Windows 10.</div>
<div> </div>

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/xaudio2fx-i3dl2-preset">XAUDIO2FX_I3DL2_PRESET</a>



<a href="/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_i3dl2_parameters">XAUDIO2FX_REVERB_I3DL2_PARAMETERS</a>



<a href="/windows/desktop/xaudio2/functions">XAudio2::Functions</a>