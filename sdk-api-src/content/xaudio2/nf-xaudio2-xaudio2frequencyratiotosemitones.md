---
UID: NF:xaudio2.XAudio2FrequencyRatioToSemitones
title: XAudio2FrequencyRatioToSemitones function (xaudio2.h)
description: Inline function that converts a frequency ratio value to a semitone value.
helpviewer_keywords: ["XAudio2FrequencyRatioToSemitones","XAudio2FrequencyRatioToSemitones function [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2frequencyratiotosemitones","xaudio2/XAudio2FrequencyRatioToSemitones"]
old-location: xaudio2\xaudio2frequencyratiotosemitones.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.xaudio2.XAudio2FrequencyRatioToSemitones(float)
ms.date: 12/05/2018
ms.keywords: XAudio2FrequencyRatioToSemitones, XAudio2FrequencyRatioToSemitones function [XAudio2 Audio Mixing APIs], xaudio2.xaudio2frequencyratiotosemitones, xaudio2/XAudio2FrequencyRatioToSemitones
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
 - XAudio2FrequencyRatioToSemitones
 - xaudio2/XAudio2FrequencyRatioToSemitones
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
 - XAudio2FrequencyRatioToSemitones
---

# XAudio2FrequencyRatioToSemitones function


## -description

Inline function that converts a frequency ratio value to a semitone value.

## -parameters

### -param FrequencyRatio [in]

Floating point value representing the frequency ratio.

## -returns

Returns a floating point value that represents the semitone.

## -remarks

You must explicitly define XAUDIO2_HELPER_FUNCTIONS in your build for this function to become available.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/functions">XAudio2 Functions</a>