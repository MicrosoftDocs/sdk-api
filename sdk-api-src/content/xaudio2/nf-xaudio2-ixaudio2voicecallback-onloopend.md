---
UID: NF:xaudio2.IXAudio2VoiceCallback.OnLoopEnd
title: IXAudio2VoiceCallback::OnLoopEnd (xaudio2.h)
description: Called when the voice reaches the end position of a loop.
helpviewer_keywords: ["IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs]","OnLoopEnd method","IXAudio2VoiceCallback.OnLoopEnd","IXAudio2VoiceCallback::OnLoopEnd","OnLoopEnd","OnLoopEnd method [XAudio2 Audio Mixing APIs]","OnLoopEnd method [XAudio2 Audio Mixing APIs]","IXAudio2VoiceCallback interface","xaudio2.ixaudio2voicecallback_interface_onloopend","xaudio2/IXAudio2VoiceCallback::OnLoopEnd"]
old-location: xaudio2\ixaudio2voicecallback_interface_onloopend.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voicecallback.IXAudio2VoiceCallback.OnLoopEnd(void)
ms.date: 12/05/2018
ms.keywords: IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs],OnLoopEnd method, IXAudio2VoiceCallback.OnLoopEnd, IXAudio2VoiceCallback::OnLoopEnd, OnLoopEnd, OnLoopEnd method [XAudio2 Audio Mixing APIs], OnLoopEnd method [XAudio2 Audio Mixing APIs],IXAudio2VoiceCallback interface, xaudio2.ixaudio2voicecallback_interface_onloopend, xaudio2/IXAudio2VoiceCallback::OnLoopEnd
f1_keywords:
- xaudio2/IXAudio2VoiceCallback.OnLoopEnd
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- xaudio2.h
api_name:
- IXAudio2VoiceCallback.OnLoopEnd
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXAudio2VoiceCallback::OnLoopEnd


## -description


Called when the voice reaches the end position of a loop.


## -parameters




### -param pBufferContext

Context pointer that was assigned to the <b>pContext</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a> structure when the buffer was submitted. 


## -remarks



<i>pBufferContext</i> is the context pointer originally provided by the <b>pContext</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer">XAUDIO2_BUFFER</a> structure, which may be NULL.



<b>OnLoopEnd</b> is not sample-accurate; that is, actions in the callback do not occur at the exact moment that a given sample is being processed. It is only guaranteed to be called shortly after the last sample in the loop has been processed.



For information about the <a href="https://docs.microsoft.com/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a> interface methods, see the <a href="https://docs.microsoft.com/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a> section.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/xaudio2/how-to--use-source-voice-callbacks">How to: Use Source Voice Callbacks</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback">IXAudio2VoiceCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a>
 

 

