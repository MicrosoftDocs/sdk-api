---
UID: NF:xaudio2.IXAudio2VoiceCallback.OnVoiceProcessingPassStart
title: IXAudio2VoiceCallback::OnVoiceProcessingPassStart (xaudio2.h)
description: Called during each processing pass for each voice, just before XAudio2 reads data from the voice's buffer queue.
helpviewer_keywords: ["IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs]","OnVoiceProcessingPassStart method","IXAudio2VoiceCallback.OnVoiceProcessingPassStart","IXAudio2VoiceCallback::OnVoiceProcessingPassStart","OnVoiceProcessingPassStart","OnVoiceProcessingPassStart method [XAudio2 Audio Mixing APIs]","OnVoiceProcessingPassStart method [XAudio2 Audio Mixing APIs]","IXAudio2VoiceCallback interface","xaudio2.ixaudio2voicecallback_interface_onvoiceprocessingpassstart","xaudio2/IXAudio2VoiceCallback::OnVoiceProcessingPassStart"]
old-location: xaudio2\ixaudio2voicecallback_interface_onvoiceprocessingpassstart.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voicecallback.IXAudio2VoiceCallback.OnVoiceProcessingPassStart(UINT32)
ms.date: 12/05/2018
ms.keywords: IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs],OnVoiceProcessingPassStart method, IXAudio2VoiceCallback.OnVoiceProcessingPassStart, IXAudio2VoiceCallback::OnVoiceProcessingPassStart, OnVoiceProcessingPassStart, OnVoiceProcessingPassStart method [XAudio2 Audio Mixing APIs], OnVoiceProcessingPassStart method [XAudio2 Audio Mixing APIs],IXAudio2VoiceCallback interface, xaudio2.ixaudio2voicecallback_interface_onvoiceprocessingpassstart, xaudio2/IXAudio2VoiceCallback::OnVoiceProcessingPassStart
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
 - IXAudio2VoiceCallback::OnVoiceProcessingPassStart
 - xaudio2/IXAudio2VoiceCallback::OnVoiceProcessingPassStart
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
 - IXAudio2VoiceCallback.OnVoiceProcessingPassStart
---

# IXAudio2VoiceCallback::OnVoiceProcessingPassStart


## -description

Called during each processing pass for each voice, just before XAudio2 reads data from the voice's buffer queue.

## -parameters

### -param BytesRequired

The number of bytes that must be submitted immediately to avoid starvation. This allows the implementation of just-in-time streaming scenarios; the client can keep the absolute minimum data queued on the voice at all times, and pass it fresh data just before the data is required. This model provides the lowest possible latency attainable with XAudio2. For xWMA and XMA data <i>BytesRequired</i> will always be zero, since the concept of a frame of xWMA or XMA data is meaningless. 

<div class="alert"><b>Note</b>  In a situation where there is always plenty of data available on the source voice, <i>BytesRequired</i> should always report zero, because it doesn't need any samples immediately to avoid glitching.</div>
<div> </div>

## -remarks

For information about <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a> interface methods, see the <a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a> topic.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--use-source-voice-callbacks">How to: Use Source Voice Callbacks</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>



<a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a>