---
UID: NF:xaudio2.IXAudio2VoiceCallback.OnBufferEnd
title: IXAudio2VoiceCallback::OnBufferEnd (xaudio2.h)
description: Called when the voice finishes processing a buffer.
helpviewer_keywords: ["IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs]","OnBufferEnd method","IXAudio2VoiceCallback.OnBufferEnd","IXAudio2VoiceCallback::OnBufferEnd","OnBufferEnd","OnBufferEnd method [XAudio2 Audio Mixing APIs]","OnBufferEnd method [XAudio2 Audio Mixing APIs]","IXAudio2VoiceCallback interface","xaudio2.ixaudio2voicecallback_interface_onbufferend","xaudio2/IXAudio2VoiceCallback::OnBufferEnd"]
old-location: xaudio2\ixaudio2voicecallback_interface_onbufferend.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voicecallback.IXAudio2VoiceCallback.OnBufferEnd(void)
ms.date: 12/05/2018
ms.keywords: IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs],OnBufferEnd method, IXAudio2VoiceCallback.OnBufferEnd, IXAudio2VoiceCallback::OnBufferEnd, OnBufferEnd, OnBufferEnd method [XAudio2 Audio Mixing APIs], OnBufferEnd method [XAudio2 Audio Mixing APIs],IXAudio2VoiceCallback interface, xaudio2.ixaudio2voicecallback_interface_onbufferend, xaudio2/IXAudio2VoiceCallback::OnBufferEnd
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
 - IXAudio2VoiceCallback::OnBufferEnd
 - xaudio2/IXAudio2VoiceCallback::OnBufferEnd
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
 - IXAudio2VoiceCallback.OnBufferEnd
---

# IXAudio2VoiceCallback::OnBufferEnd


## -description

Called when the voice finishes processing a buffer.

## -parameters

### -param pBufferContext

Context pointer assigned to the <b>pContext</b> member of the <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a> structure when the buffer was submitted.

## -remarks

After an <b>OnBufferEnd</b> callback the audio memory for the buffer associated with <i>pBufferContext</i> can safely be released.



<i>pBufferContext</i> is the context pointer originally provided by the <b>pContext </b> member of the <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a> structure, which may be NULL.



<b>OnBufferEnd</b> is guaranteed to be called just after the last byte of the current buffer has been consumed and before the first byte of the next buffer is consumed. This callback can be used to overwrite or release the audio data referenced by the completed buffer, and to update other state associated with the voice as appropriate.



For information about <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a> interface methods, see the <a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a> topic.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--stream-a-sound-from-disk">How to: Stream a Sound from Disk</a>



<a href="/windows/desktop/xaudio2/how-to--use-source-voice-callbacks">How to: Use Source Voice Callbacks</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>