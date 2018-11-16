---
UID: NF:xaudio2.IXAudio2VoiceCallback.OnStreamEnd
title: IXAudio2VoiceCallback::OnStreamEnd
author: windows-sdk-content
description: Called when the voice has just finished playing a contiguous audio stream.
old-location: xaudio2\ixaudio2voicecallback_interface_onstreamend.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voicecallback.IXAudio2VoiceCallback.OnStreamEnd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs],OnStreamEnd method, IXAudio2VoiceCallback.OnStreamEnd, IXAudio2VoiceCallback::OnStreamEnd, OnStreamEnd, OnStreamEnd method [XAudio2 Audio Mixing APIs], OnStreamEnd method [XAudio2 Audio Mixing APIs],IXAudio2VoiceCallback interface, xaudio2.ixaudio2voicecallback_interface_onstreamend, xaudio2/IXAudio2VoiceCallback::OnStreamEnd
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
 - IXAudio2VoiceCallback.OnStreamEnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xaudio2.h
: 
- IXAudio2VoiceCallback.OnStreamEnd
: 
---

# IXAudio2VoiceCallback::OnStreamEnd


## -description


Called when the voice has just finished playing a contiguous audio stream.


## -parameters






## -returns



This method does not return a value.




## -remarks



<b>OnStreamEnd</b> is triggered when XAudio2 processes an <a href="https://msdn.microsoft.com/b6c2a08b-6abb-4e6a-8acb-6f8983aef95f">XAUDIO2_BUFFER</a> with the XAUDIO2_END_OF_STREAM flag set. See the <a href="https://msdn.microsoft.com/D4A1FB27-12F6-41A0-9ACF-3F13EBB27165">IXAudio2SourceVoice::SubmitSourceBuffer</a> method for more information.



The <b>OnStreamEnd</b> callback indicates that XAudio2 has finished consuming the last buffer submitted to the voice. With PCM data, all audio is guaranteed to have been played and the voice can be stopped or destroyed safely. 



The <b>OnStreamEnd</b> callback only indicates that an <a href="https://msdn.microsoft.com/b6c2a08b-6abb-4e6a-8acb-6f8983aef95f">XAUDIO2_BUFFER</a> with the XAUDIO2_END_OF_STREAM flag set has been processed. The callback is strictly informational and does not change the state of the source voice that triggered it. A voice stays in the start state until <a href="https://msdn.microsoft.com/A46CF7D1-5BBD-45F2-9C2A-90FE51A6FA75">IXAudio2SourceVoice::Stop</a>    is called and will continue to play submitted source buffers and to trigger additional callbacks.



<b>OnStreamEnd</b> is guaranteed to be called just after the last byte of the current buffer has been consumed.



For information about <a href="https://msdn.microsoft.com/FF78727D-16AE-40CB-BDE0-664687914FC0">IXAudio2VoiceCallback</a> interface methods, see the <a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a> topic.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/0bace0c5-9171-efd8-9a38-2c2b3452f73f">How to: Use Source Voice Callbacks</a>



<a href="https://msdn.microsoft.com/FF78727D-16AE-40CB-BDE0-664687914FC0">IXAudio2VoiceCallback</a>



<a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a>
 

 

