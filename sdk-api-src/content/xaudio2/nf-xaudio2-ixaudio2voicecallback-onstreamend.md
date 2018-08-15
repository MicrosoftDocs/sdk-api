---
UID: NF:xaudio2.IXAudio2VoiceCallback.OnStreamEnd
title: IXAudio2VoiceCallback::OnStreamEnd
author: windows-sdk-content
description: Called when the voice has just finished playing a contiguous audio stream.
old-location: xaudio2\ixaudio2voicecallback_interface_onstreamend.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voicecallback.IXAudio2VoiceCallback.OnStreamEnd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs],OnStreamEnd method, IXAudio2VoiceCallback.OnStreamEnd, IXAudio2VoiceCallback::OnStreamEnd, OnStreamEnd, OnStreamEnd method [XAudio2 Audio Mixing APIs], OnStreamEnd method [XAudio2 Audio Mixing APIs],IXAudio2VoiceCallback interface, xaudio2.ixaudio2voicecallback_interface_onstreamend, xaudio2/IXAudio2VoiceCallback::OnStreamEnd
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xaudio2.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: XAUDIO2_FILTER_TYPE
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
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAudio2VoiceCallback::OnStreamEnd


## -description


Called when the voice has just finished playing a contiguous audio stream.


## -parameters






## -returns



This method does not return a value.




## -remarks



<b>OnStreamEnd</b> is triggered when XAudio2 processes an <a href="https://msdn.microsoft.com/en-us/library/Ee419228(v=VS.85).aspx">XAUDIO2_BUFFER</a> with the XAUDIO2_END_OF_STREAM flag set. See the <a href="https://msdn.microsoft.com/en-us/library/Ee418473(v=VS.85).aspx">IXAudio2SourceVoice::SubmitSourceBuffer</a> method for more information.



The <b>OnStreamEnd</b> callback indicates that XAudio2 has finished consuming the last buffer submitted to the voice. With PCM data, all audio is guaranteed to have been played and the voice can be stopped or destroyed safely. 



The <b>OnStreamEnd</b> callback only indicates that an <a href="https://msdn.microsoft.com/en-us/library/Ee419228(v=VS.85).aspx">XAUDIO2_BUFFER</a> with the XAUDIO2_END_OF_STREAM flag set has been processed. The callback is strictly informational and does not change the state of the source voice that triggered it. A voice stays in the start state until <a href="https://msdn.microsoft.com/en-us/library/Ee418472(v=VS.85).aspx">IXAudio2SourceVoice::Stop</a>    is called and will continue to play submitted source buffers and to trigger additional callbacks.



<b>OnStreamEnd</b> is guaranteed to be called just after the last byte of the current buffer has been consumed.



For information about <a href="https://msdn.microsoft.com/en-us/library/Ee415919(v=VS.85).aspx">IXAudio2VoiceCallback</a> interface methods, see the <a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a> topic.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/0bace0c5-9171-efd8-9a38-2c2b3452f73f">How to: Use Source Voice Callbacks</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415919(v=VS.85).aspx">IXAudio2VoiceCallback</a>



<a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a>
 

 

