---
UID: NF:xaudio2.IXAudio2VoiceCallback.OnBufferEnd
title: IXAudio2VoiceCallback::OnBufferEnd
author: windows-sdk-content
description: Called when the voice finishes processing a buffer.
old-location: xaudio2\ixaudio2voicecallback_interface_onbufferend.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voicecallback.IXAudio2VoiceCallback.OnBufferEnd(void)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs],OnBufferEnd method, IXAudio2VoiceCallback.OnBufferEnd, IXAudio2VoiceCallback::OnBufferEnd, OnBufferEnd, OnBufferEnd method [XAudio2 Audio Mixing APIs], OnBufferEnd method [XAudio2 Audio Mixing APIs],IXAudio2VoiceCallback interface, xaudio2.ixaudio2voicecallback_interface_onbufferend, xaudio2/IXAudio2VoiceCallback::OnBufferEnd
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IXAudio2VoiceCallback.OnBufferEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXAudio2VoiceCallback::OnBufferEnd


## -description


Called when the voice finishes processing a buffer. 


## -parameters




### -param pBufferContext

Context pointer assigned to the <b>pContext</b> member of the <a href="https://msdn.microsoft.com/b6c2a08b-6abb-4e6a-8acb-6f8983aef95f">XAUDIO2_BUFFER</a> structure when the buffer was submitted.


## -returns



This method does not return a value.




## -remarks



After an <b>OnBufferEnd</b> callback the audio memory for the buffer associated with <i>pBufferContext</i> can safely be released.



<i>pBufferContext</i> is the context pointer originally provided by the <b>pContext </b>member of the <a href="https://msdn.microsoft.com/b6c2a08b-6abb-4e6a-8acb-6f8983aef95f">XAUDIO2_BUFFER</a> structure, which may be NULL.



<b>OnBufferEnd</b> is guaranteed to be called just after the last byte of the current buffer has been consumed and before the first byte of the next buffer is consumed. This callback can be used to overwrite or release the audio data referenced by the completed buffer, and to update other state associated with the voice as appropriate.



For information about <a href="https://msdn.microsoft.com/FF78727D-16AE-40CB-BDE0-664687914FC0">IXAudio2VoiceCallback</a> interface methods, see the <a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a> topic.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/48b80a66-91c1-973f-069b-6f63422d7154">How to: Stream a Sound from Disk</a>



<a href="https://msdn.microsoft.com/0bace0c5-9171-efd8-9a38-2c2b3452f73f">How to: Use Source Voice Callbacks</a>



<a href="https://msdn.microsoft.com/FF78727D-16AE-40CB-BDE0-664687914FC0">IXAudio2VoiceCallback</a>
 

 

