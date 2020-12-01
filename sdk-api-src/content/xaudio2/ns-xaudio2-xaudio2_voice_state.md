---
UID: NS:xaudio2.XAUDIO2_VOICE_STATE
title: XAUDIO2_VOICE_STATE (xaudio2.h)
description: Returns the voice's current state and cursor position data.
helpviewer_keywords: ["XAUDIO2_VOICE_STATE","XAUDIO2_VOICE_STATE structure [XAudio2 Audio Mixing APIs]","xaudio2.xaudio2_voice_state","xaudio2/XAUDIO2_VOICE_STATE"]
old-location: xaudio2\xaudio2_voice_state.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_VOICE_STATE
ms.date: 12/05/2018
ms.keywords: XAUDIO2_VOICE_STATE, XAUDIO2_VOICE_STATE structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_voice_state, xaudio2/XAUDIO2_VOICE_STATE
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
req.typenames: XAUDIO2_VOICE_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAUDIO2_VOICE_STATE
 - xaudio2/XAUDIO2_VOICE_STATE
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
 - XAUDIO2_VOICE_STATE
---

# XAUDIO2_VOICE_STATE structure


## -description

Returns the voice's current state and cursor position data.

## -struct-fields

### -field pCurrentBufferContext

Pointer to a buffer context provided in the <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a> that is processed currently, or, if the voice is stopped currently, to the next buffer due to be processed. <b>pCurrentBufferContext</b> is NULL if there are no buffers in the queue.

### -field BuffersQueued

Number of audio buffers currently queued on the voice, including the one that is processed currently.

### -field SamplesPlayed

Total number of samples processed by this voice since it last started, or since the last audio stream ended (as marked with the XAUDIO2_END_OF_STREAM flag). This total includes samples played multiple times due to looping. Theoretically, if all audio emitted by the voice up to this time is captured, this parameter would be the length of the audio stream in samples. If you specify <b>XAUDIO2_VOICE_NOSAMPLESPLAYED</b> when you call <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate">IXAudio2SourceVoice::GetState</a>, this member won't be calculated, and its value is unspecified on return from <b>IXAudio2SourceVoice::GetState</b>. <b>IXAudio2SourceVoice::GetState</b> takes about one-third as much time to complete when you specify <b>XAUDIO2_VOICE_NOSAMPLESPLAYED</b>.

## -remarks

For all encoded formats, including constant bit rate (CBR) formats such as adaptive differential pulse code modulation (ADPCM), <b>SamplesPlayed</b> is expressed in terms of decoded samples. For pulse code modulation (PCM) formats, <b>SamplesPlayed</b> is expressed in terms of either input or output samples. There is a one-to-one mapping from input to output for PCM formats.



If a client needs to get the correlated positions of several voices—that is, to know exactly which sample of a particular voice is playing when a specified sample of another voice is playing—it must make the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate">IXAudio2SourceVoice::GetState</a> calls in an XAudio2 engine callback. Doing this ensures that none of the voices advance while the calls are made.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>