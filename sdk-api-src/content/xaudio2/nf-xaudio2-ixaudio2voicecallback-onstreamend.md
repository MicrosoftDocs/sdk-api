---
UID: NF:xaudio2.IXAudio2VoiceCallback.OnStreamEnd
title: IXAudio2VoiceCallback::OnStreamEnd (xaudio2.h)
description: Called when the voice has just finished playing a contiguous audio stream.
helpviewer_keywords: ["IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs]","OnStreamEnd method","IXAudio2VoiceCallback.OnStreamEnd","IXAudio2VoiceCallback::OnStreamEnd","OnStreamEnd","OnStreamEnd method [XAudio2 Audio Mixing APIs]","OnStreamEnd method [XAudio2 Audio Mixing APIs]","IXAudio2VoiceCallback interface","xaudio2.ixaudio2voicecallback_interface_onstreamend","xaudio2/IXAudio2VoiceCallback::OnStreamEnd"]
old-location: xaudio2\ixaudio2voicecallback_interface_onstreamend.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voicecallback.IXAudio2VoiceCallback.OnStreamEnd
ms.date: 12/05/2018
ms.keywords: IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs],OnStreamEnd method, IXAudio2VoiceCallback.OnStreamEnd, IXAudio2VoiceCallback::OnStreamEnd, OnStreamEnd, OnStreamEnd method [XAudio2 Audio Mixing APIs], OnStreamEnd method [XAudio2 Audio Mixing APIs],IXAudio2VoiceCallback interface, xaudio2.ixaudio2voicecallback_interface_onstreamend, xaudio2/IXAudio2VoiceCallback::OnStreamEnd
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
 - IXAudio2VoiceCallback::OnStreamEnd
 - xaudio2/IXAudio2VoiceCallback::OnStreamEnd
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
 - IXAudio2VoiceCallback.OnStreamEnd
---

# IXAudio2VoiceCallback::OnStreamEnd


## -description

Called when the voice has just finished playing a contiguous audio stream.



## -remarks

<b>OnStreamEnd</b> is triggered when XAudio2 processes an <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a> with the XAUDIO2_END_OF_STREAM flag set. See the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer">IXAudio2SourceVoice::SubmitSourceBuffer</a> method for more information.



The <b>OnStreamEnd</b> callback indicates that XAudio2 has finished consuming the last buffer submitted to the voice. With PCM data, all audio is guaranteed to have been played and the voice can be stopped or destroyed safely. 



The <b>OnStreamEnd</b> callback only indicates that an <a href="/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a> with the XAUDIO2_END_OF_STREAM flag set has been processed. The callback is strictly informational and does not change the state of the source voice that triggered it. A voice stays in the start state until <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop">IXAudio2SourceVoice::Stop</a>    is called and will continue to play submitted source buffers and to trigger additional callbacks.



<b>OnStreamEnd</b> is guaranteed to be called just after the last byte of the current buffer has been consumed.



For information about <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a> interface methods, see the <a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a> topic.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--use-source-voice-callbacks">How to: Use Source Voice Callbacks</a>



<a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>



<a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a>
