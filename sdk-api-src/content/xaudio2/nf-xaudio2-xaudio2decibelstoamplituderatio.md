---
UID: NF:xaudio2.XAudio2DecibelsToAmplitudeRatio
title: XAudio2DecibelsToAmplitudeRatio function (xaudio2.h)
description: Inline function that converts a decibel value to an amplitude ratio value.
helpviewer_keywords: ["XAudio2DecibelsToAmplitudeRatio","XAudio2DecibelsToAmplitudeRatio function [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2decibelstoamplituderatio","xaudio2/XAudio2DecibelsToAmplitudeRatio"]
old-location: xaudio2\xaudio2decibelstoamplituderatio.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xaudio2.XAudio2DecibelsToAmplitudeRatio(float)
ms.date: 12/05/2018
ms.keywords: XAudio2DecibelsToAmplitudeRatio, XAudio2DecibelsToAmplitudeRatio function [XAudio2 Audio Mixing APIs], xaudio2.xaudio2decibelstoamplituderatio, xaudio2/XAudio2DecibelsToAmplitudeRatio
req.header: xaudio2.h
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
 - XAudio2DecibelsToAmplitudeRatio
 - xaudio2/XAudio2DecibelsToAmplitudeRatio
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xaudio2.h
api_name:
 - XAudio2DecibelsToAmplitudeRatio
---

# XAudio2DecibelsToAmplitudeRatio function


## -description

Inline function that converts a decibel value to an amplitude ratio value.

## -parameters

### -param Decibels [in]

Floating point value representing the decibel level.

## -returns

Returns a floating point value that represents the amplitude ratio.

## -remarks

This function can be used to calculate the Volume parameter value passed to the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume">IXAudio2Voice::SetVolume</a> function.



You must explicitly define XAUDIO2_HELPER_FUNCTIONS in your build for this function to become available.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/functions">XAudio2 Functions</a>