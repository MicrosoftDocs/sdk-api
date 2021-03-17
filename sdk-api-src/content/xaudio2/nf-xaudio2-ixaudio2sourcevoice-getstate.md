---
UID: NF:xaudio2.IXAudio2SourceVoice.GetState
title: IXAudio2SourceVoice::GetState (xaudio2.h)
description: Returns the voice's current cursor position data.
helpviewer_keywords: ["GetState","GetState method [XAudio2 Audio Mixing APIs]","GetState method [XAudio2 Audio Mixing APIs]","IXAudio2SourceVoice interface","IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs]","GetState method","IXAudio2SourceVoice.GetState","IXAudio2SourceVoice::GetState","xaudio2.ixaudio2sourcevoice_interface_getstate","xaudio2/IXAudio2SourceVoice::GetState"]
old-location: xaudio2\ixaudio2sourcevoice_interface_getstate.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice.GetState(XAUDIO2_VOICE_STATE,UINT32)
ms.date: 12/05/2018
ms.keywords: GetState, GetState method [XAudio2 Audio Mixing APIs], GetState method [XAudio2 Audio Mixing APIs],IXAudio2SourceVoice interface, IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],GetState method, IXAudio2SourceVoice.GetState, IXAudio2SourceVoice::GetState, xaudio2.ixaudio2sourcevoice_interface_getstate, xaudio2/IXAudio2SourceVoice::GetState
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
 - IXAudio2SourceVoice::GetState
 - xaudio2/IXAudio2SourceVoice::GetState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2SourceVoice.GetState
---

# IXAudio2SourceVoice::GetState


## -description

Returns the voice's current cursor position data.

## -parameters

### -param pVoiceState

Pointer to an <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_state">XAUDIO2_VOICE_STATE</a> structure containing the state of the voice.

### -param X2DEFAULT

TBD

### -param Flags [optional]

Flags controlling which voice state data should be returned. Valid values are 0 or <b>XAUDIO2_VOICE_NOSAMPLESPLAYED</b>. The default value is 0. If you specify <b>XAUDIO2_VOICE_NOSAMPLESPLAYED</b>, <b>GetState</b> returns only the buffer state, not the sampler state. <b>GetState</b> takes roughly one-third as much time to complete when you specify 
<b>XAUDIO2_VOICE_NOSAMPLESPLAYED</b>.

## -remarks

If a client needs to get the correlated positions of several voices (for example, to know exactly which sample of a given voice is playing when a given sample of another voice is playing), it must make <b>GetState</b> calls in an XAudio2 engine callback. This ensures that none of the voices advance while the calls are being made. See the <a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a> overview for information about using XAudio2 callbacks.



Note that the DirectX SDK versions of XAUDIO2 do not take the Flags parameter for <b>GetState</b>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--stream-a-sound-from-disk">How to: Stream a Sound from Disk</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice">IXAudio2SourceVoice</a>