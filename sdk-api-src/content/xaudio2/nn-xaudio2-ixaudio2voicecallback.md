---
UID: NN:xaudio2.IXAudio2VoiceCallback
title: IXAudio2VoiceCallback (xaudio2.h)
description: The IXAudio2VoiceCallback interface contains methods that notify the client when certain events happen in a given IXAudio2SourceVoice.
helpviewer_keywords: ["IXAudio2VoiceCallback","IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs]","IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs]","described","xaudio2.ixaudio2voicecallback","xaudio2/IXAudio2VoiceCallback"]
old-location: xaudio2\ixaudio2voicecallback.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.ixaudio2voicecallback.IXAudio2VoiceCallback
ms.date: 12/05/2018
ms.keywords: IXAudio2VoiceCallback, IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs], IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs],described, xaudio2.ixaudio2voicecallback, xaudio2/IXAudio2VoiceCallback
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
req.lib: Xaudio2.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXAudio2VoiceCallback
 - xaudio2/IXAudio2VoiceCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.lib
 - xaudio2.dll
api_name:
 - IXAudio2VoiceCallback
---

# IXAudio2VoiceCallback interface


## -description

The <b>IXAudio2VoiceCallback</b> interface contains methods that notify the client when certain events happen in a given <a href="/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice">IXAudio2SourceVoice</a>. 

This interface should be implemented by the XAudio2 client. XAudio2 calls these methods through an interface pointer provided by the client in the <a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice">IXAudio2::CreateSourceVoice</a> method. Methods in this interface return void, rather than an HRESULT. 


See the <a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a> topic for restrictions on callback implementation.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend">OnBufferEnd</a>
</td>
<td align="left" width="63%">
Called when the voice finishes processing a buffer. 

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferstart">OnBufferStart</a>
</td>
<td align="left" width="63%">
Called when the voice is about to start processing a new audio buffer.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onloopend">OnLoopEnd</a>
</td>
<td align="left" width="63%">
Called when the voice reaches the end position of a loop.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend">OnStreamEnd</a>
</td>
<td align="left" width="63%">
Called when the voice has just finished playing a contiguous audio stream.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onvoiceerror">OnVoiceError</a>
</td>
<td align="left" width="63%">
Called when a critical error occurs during voice processing.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onvoiceprocessingpassend">OnVoiceProcessingPassEnd</a>
</td>
<td align="left" width="63%">
Called just after the processing pass for the voice ends.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onvoiceprocessingpassstart">OnVoiceProcessingPassStart</a>
</td>
<td align="left" width="63%">
Called during each processing pass for each voice, just before XAudio2 reads data from the voice's buffer queue.

</td>
</tr>
</table>

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/how-to--stream-a-sound-from-disk">How to: Stream a Sound from Disk</a>



<a href="/windows/desktop/xaudio2/how-to--use-source-voice-callbacks">How to: Use Source Voice Callbacks</a>



<a href="/windows/desktop/xaudio2/xaudio2-callbacks">XAudio2 Callbacks</a>



<a href="/windows/desktop/xaudio2/interfaces">XAudio2 Interfaces</a>
