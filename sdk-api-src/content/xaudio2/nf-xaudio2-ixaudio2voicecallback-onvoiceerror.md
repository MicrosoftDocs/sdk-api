---
UID: NF:xaudio2.IXAudio2VoiceCallback.OnVoiceError
title: IXAudio2VoiceCallback::OnVoiceError (xaudio2.h)
author: windows-sdk-content
description: Called when a critical error occurs during voice processing.
old-location: xaudio2\ixaudio2voicecallback_interface_onvoiceerror.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voicecallback.IXAudio2VoiceCallback.OnVoiceError(void,HRESULT)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs],OnVoiceError method, IXAudio2VoiceCallback.OnVoiceError, IXAudio2VoiceCallback::OnVoiceError, OnVoiceError, OnVoiceError method [XAudio2 Audio Mixing APIs], OnVoiceError method [XAudio2 Audio Mixing APIs],IXAudio2VoiceCallback interface, xaudio2.ixaudio2voicecallback_interface_onvoiceerror, xaudio2/IXAudio2VoiceCallback::OnVoiceError
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
 - IXAudio2VoiceCallback.OnVoiceError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXAudio2VoiceCallback::OnVoiceError


## -description


Called when a critical error occurs during voice processing.


## -parameters




### -param pBufferContext

Context pointer that was assigned to the <b>pContext</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Ee419228(v=VS.85).aspx">XAUDIO2_BUFFER</a> structure when the buffer was submitted.


### -param Error

The HRESULT code of the error encountered.


## -returns



This method does not return a value.




## -remarks



<b>OnVoiceError</b> is called in the event of an error during voice processing, such as a hardware XMA decoder error on the Xbox 360. The arguments report which buffer was being processed at the time of the error, and its HRESULT code. If the error is not recoverable by destroying and re-creating the voice, the <a href="https://msdn.microsoft.com/en-us/library/Ee418461(v=VS.85).aspx">OnCriticalError</a> engine callback will be called as well. 


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/0bace0c5-9171-efd8-9a38-2c2b3452f73f">How to: Use Source Voice Callbacks</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415919(v=VS.85).aspx">IXAudio2VoiceCallback</a>



<a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a>
 

 

