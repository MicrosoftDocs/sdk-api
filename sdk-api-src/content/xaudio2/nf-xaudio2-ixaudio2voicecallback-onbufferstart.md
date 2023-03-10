---
UID: NF:xaudio2.IXAudio2VoiceCallback.OnBufferStart
title: IXAudio2VoiceCallback::OnBufferStart (xaudio2.h)
description: Called when the voice is about to start processing a new audio buffer.
helpviewer_keywords: ["IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs]","OnBufferStart method","IXAudio2VoiceCallback.OnBufferStart","IXAudio2VoiceCallback::OnBufferStart","OnBufferStart","OnBufferStart method [XAudio2 Audio Mixing APIs]","OnBufferStart method [XAudio2 Audio Mixing APIs]","IXAudio2VoiceCallback interface","xaudio2.ixaudio2voicecallback_interface_onbufferstart","xaudio2/IXAudio2VoiceCallback::OnBufferStart"]
old-location: xaudio2\ixaudio2voicecallback_interface_onbufferstart.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voicecallback.IXAudio2VoiceCallback.OnBufferStart(void)
ms.date: 12/05/2018
ms.keywords: IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs],OnBufferStart method, IXAudio2VoiceCallback.OnBufferStart, IXAudio2VoiceCallback::OnBufferStart, OnBufferStart, OnBufferStart method [XAudio2 Audio Mixing APIs], OnBufferStart method [XAudio2 Audio Mixing APIs],IXAudio2VoiceCallback interface, xaudio2.ixaudio2voicecallback_interface_onbufferstart, xaudio2/IXAudio2VoiceCallback::OnBufferStart
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
 - IXAudio2VoiceCallback::OnBufferStart
 - xaudio2/IXAudio2VoiceCallback::OnBufferStart
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
 - IXAudio2VoiceCallback.OnBufferStart
---

# IXAudio2VoiceCallback::OnBufferStart


## -description

Called when the voice is about to start processing a new audio buffer.

## -parameters

### -param pBufferContext

Context pointer that was assigned to the pContext member of the <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a> structure when the buffer was submitted.

## -remarks

<i>pBufferContext</i> is the context pointer originally provided by the <b>pContext</b> member of the <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a> structure, which may be NULL.



<b>OnBufferStart</b> is guaranteed to be called just before the first byte of the current buffer is consumed. It is appropriate to use this callback for changes to the voice state such as the following.

<ul>
<li>Submitting a new buffer to the voice

</li>
<li>Adjusting the volume, pitch, and effect parameters of the voice

</li>
<li>Enabling or disabling an effect in the voice's effect chain</li>
</ul>All the actions listed above are synchronous when performed in an XAudio2 callback, so the changes will take effect immediately, affecting the buffer that is about to start.



It is also safe to use this callback to write audio data to the buffer directly, which can be useful for low-latency streaming scenarios. However, as with all XAudio2 callbacks, no work should be done that uses a significant amount of processor time or could block execution, including synchronous disk or network reads.



For information about the <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a> interface methods, see the <a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a> section.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--use-source-voice-callbacks">How to: Use Source Voice Callbacks</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>



<a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a>