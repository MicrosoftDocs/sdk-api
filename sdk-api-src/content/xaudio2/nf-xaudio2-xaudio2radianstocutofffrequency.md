---
UID: NF:xaudio2.XAudio2RadiansToCutoffFrequency
title: XAudio2RadiansToCutoffFrequency function (xaudio2.h)
description: Inline function that converts from the radian frequencies used in XAUDIO2_FILTER_PARAMETERS back to absolute frequencies in hertz.
helpviewer_keywords: ["XAudio2RadiansToCutoffFrequency","XAudio2RadiansToCutoffFrequency function [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2radianstocutofffrequency","xaudio2/XAudio2RadiansToCutoffFrequency"]
old-location: xaudio2\xaudio2radianstocutofffrequency.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xaudio2.XAudio2RadiansToCutoffFrequency(float,float)
ms.date: 12/05/2018
ms.keywords: XAudio2RadiansToCutoffFrequency, XAudio2RadiansToCutoffFrequency function [XAudio2 Audio Mixing APIs], xaudio2.xaudio2radianstocutofffrequency, xaudio2/XAudio2RadiansToCutoffFrequency
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
 - XAudio2RadiansToCutoffFrequency
 - xaudio2/XAudio2RadiansToCutoffFrequency
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
 - XAudio2RadiansToCutoffFrequency
---

# XAudio2RadiansToCutoffFrequency function


## -description

Inline function that converts from the radian frequencies used in <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters">XAUDIO2_FILTER_PARAMETERS</a> back to absolute frequencies in hertz.

## -parameters

### -param Radians [in]

Value of the Frequency member of the <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters">XAUDIO2_FILTER_PARAMETERS</a> structure.

### -param SampleRate [in]

The sample rate of the audio data affected by the <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters">XAUDIO2_FILTER_PARAMETERS</a> structure.

## -returns

Returns a floating-point value that represents the frequency in hertz.

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/functions">XAudio2 Functions</a>