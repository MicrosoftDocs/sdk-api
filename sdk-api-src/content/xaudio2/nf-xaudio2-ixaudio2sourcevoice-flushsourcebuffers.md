---
UID: NF:xaudio2.IXAudio2SourceVoice.FlushSourceBuffers
title: IXAudio2SourceVoice::FlushSourceBuffers (xaudio2.h)
description: Removes all pending audio buffers from the voice queue.
helpviewer_keywords: ["FlushSourceBuffers","FlushSourceBuffers method [XAudio2 Audio Mixing APIs]","FlushSourceBuffers method [XAudio2 Audio Mixing APIs]","IXAudio2SourceVoice interface","IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs]","FlushSourceBuffers method","IXAudio2SourceVoice.FlushSourceBuffers","IXAudio2SourceVoice::FlushSourceBuffers","xaudio2.ixaudio2sourcevoice_interface_flushsourcebuffers","xaudio2/IXAudio2SourceVoice::FlushSourceBuffers"]
old-location: xaudio2\ixaudio2sourcevoice_interface_flushsourcebuffers.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice.FlushSourceBuffers
ms.date: 12/05/2018
ms.keywords: FlushSourceBuffers, FlushSourceBuffers method [XAudio2 Audio Mixing APIs], FlushSourceBuffers method [XAudio2 Audio Mixing APIs],IXAudio2SourceVoice interface, IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],FlushSourceBuffers method, IXAudio2SourceVoice.FlushSourceBuffers, IXAudio2SourceVoice::FlushSourceBuffers, xaudio2.ixaudio2sourcevoice_interface_flushsourcebuffers, xaudio2/IXAudio2SourceVoice::FlushSourceBuffers
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
 - IXAudio2SourceVoice::FlushSourceBuffers
 - xaudio2/IXAudio2SourceVoice::FlushSourceBuffers
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
 - IXAudio2SourceVoice.FlushSourceBuffers
---

# IXAudio2SourceVoice::FlushSourceBuffers


## -description

Removes all pending audio buffers from the voice queue.



## -returns

Returns S_OK if successful, an error code otherwise.

## -remarks

If the voice is started, the buffer that is currently playing is not removed from the queue.



<b>FlushSourceBuffers</b> can be called regardless of whether the voice is currently started or stopped.



For every buffer removed, an <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend">OnBufferEnd</a> callback will be made, but none of the other per-buffer callbacks (<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferstart">OnBufferStart</a>, <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend">OnStreamEnd</a> or <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onloopend">OnLoopEnd</a>) will be made.



<b>FlushSourceBuffers</b> does not change a the voice's running state, so if the voice was playing a buffer prior to the call, it will continue to do so, and will deliver all the callbacks for the buffer normally. This means that the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend">OnBufferEnd</a> callback for this buffer will take place after the <b>OnBufferEnd</b> callbacks for the buffers that were removed. Thus, an XAudio2 client that calls <b>FlushSourceBuffers</b> cannot expect to receive <b>OnBufferEnd</b> callbacks in the order in which the buffers were submitted.



No warnings for starvation of the buffer queue will be emitted when the currently playing buffer completes; it is assumed that the client has intentionally removed the buffers that followed it. However, there may be an audio pop if this buffer does not end at a zero crossing. If the application must ensure that the flush operation takes place while a specific buffer is playing—perhaps because the buffer ends with a zero crossing—it must call <b>FlushSourceBuffers</b> from a callback, so that it executes synchronously.



Calling <b>FlushSourceBuffers</b> after a voice is stopped and then submitting new data to the voice resets all of the voice's internal counters.



A voice's state is not considered reset after calling <b>FlushSourceBuffers</b> until the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend">OnBufferEnd</a> callback occurs (if a buffer was previously submitted) or <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate">IXAudio2SourceVoice::GetState</a> returns with <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_state">XAUDIO2_VOICE_STATE</a>. <b>BuffersQueued</b> == 0. For example, if you stop a voice and call <b>FlushSourceBuffers</b>, it's still not legal to immediately call <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setsourcesamplerate">IXAudio2SourceVoice::SetSourceSampleRate</a> (which requires the voice to not have any buffers currently queued), until either of the previously mentioned conditions are met. 



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice">IXAudio2SourceVoice</a>
