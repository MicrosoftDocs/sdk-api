---
UID: NF:xaudio2.IXAudio2VoiceCallback.OnLoopEnd
title: IXAudio2VoiceCallback::OnLoopEnd
author: windows-sdk-content
description: Called when the voice reaches the end position of a loop.
old-location: xaudio2\ixaudio2voicecallback_interface_onloopend.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voicecallback.IXAudio2VoiceCallback.OnLoopEnd(void)
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXAudio2VoiceCallback interface [XAudio2 Audio Mixing APIs],OnLoopEnd method, IXAudio2VoiceCallback.OnLoopEnd, IXAudio2VoiceCallback::OnLoopEnd, OnLoopEnd, OnLoopEnd method [XAudio2 Audio Mixing APIs], OnLoopEnd method [XAudio2 Audio Mixing APIs],IXAudio2VoiceCallback interface, xaudio2.ixaudio2voicecallback_interface_onloopend, xaudio2/IXAudio2VoiceCallback::OnLoopEnd
ms.prod: windows
ms.technology: windows-sdk
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
 - IXAudio2VoiceCallback.OnLoopEnd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAudio2VoiceCallback::OnLoopEnd


## -description


Called when the voice reaches the end position of a loop.


## -parameters




### -param pBufferContext

Context pointer that was assigned to the <b>pContext</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Ee419228(v=VS.85).aspx">XAUDIO2_BUFFER</a> structure when the buffer was submitted. 


## -returns



This method does not return a value.




## -remarks



<i>pBufferContext</i> is the context pointer originally provided by the <b>pContext</b> member of the <a href="https://msdn.microsoft.com/en-us/library/Ee419228(v=VS.85).aspx">XAUDIO2_BUFFER</a> structure, which may be NULL.



<b>OnLoopEnd</b> is not sample-accurate; that is, actions in the callback do not occur at the exact moment that a given sample is being processed. It is only guaranteed to be called shortly after the last sample in the loop has been processed.



For information about the <a href="https://msdn.microsoft.com/en-us/library/Ee415919(v=VS.85).aspx">IXAudio2VoiceCallback</a> interface methods, see the <a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a> section.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/0bace0c5-9171-efd8-9a38-2c2b3452f73f">How to: Use Source Voice Callbacks</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee415919(v=VS.85).aspx">IXAudio2VoiceCallback</a>



<a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a>
 

 

