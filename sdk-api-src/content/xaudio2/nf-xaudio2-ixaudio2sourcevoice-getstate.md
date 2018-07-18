---
UID: NF:xaudio2.IXAudio2SourceVoice.GetState
title: IXAudio2SourceVoice::GetState
author: windows-sdk-content
description: Returns the voice's current cursor position data.
old-location: xaudio2\ixaudio2sourcevoice_interface_getstate.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice.GetState(XAUDIO2_VOICE_STATE,UINT32)
ms.author: windowssdkdev
ms.date: 04/23/2018
ms.keywords: GetState, GetState method [XAudio2 Audio Mixing APIs], GetState method [XAudio2 Audio Mixing APIs],IXAudio2SourceVoice interface, IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],GetState method, IXAudio2SourceVoice.GetState, IXAudio2SourceVoice::GetState, xaudio2.ixaudio2sourcevoice_interface_getstate, xaudio2/IXAudio2SourceVoice::GetState
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
 - IXAudio2SourceVoice.GetState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAudio2SourceVoice::GetState


## -description


Returns the voice's current cursor position data.


## -parameters




### -param pVoiceState


Pointer to an <a href="https://msdn.microsoft.com/library/Ee419247(v=VS.85).aspx">XAUDIO2_VOICE_STATE</a> structure containing the state of the voice.


### -param X2DEFAULT






#### - Flags [optional]

Flags controlling which voice state data should be returned. Valid values are 0 or <b>XAUDIO2_VOICE_NOSAMPLESPLAYED</b>. The default value is 0. If you specify <b>XAUDIO2_VOICE_NOSAMPLESPLAYED</b>, <b>GetState</b> returns only the buffer state, not the sampler state. <b>GetState</b> takes roughly one-third as much time to complete when you specify 
<b>XAUDIO2_VOICE_NOSAMPLESPLAYED</b>.


## -returns



This method does not return a value.




## -remarks



If a client needs to get the correlated positions of several voices (for example, to know exactly which sample of a given voice is playing when a given sample of another voice is playing), it must make <b>GetState</b> calls in an XAudio2 engine callback. This ensures that none of the voices advance while the calls are being made. See the <a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a> overview for information about using XAudio2 callbacks.



Note that the DirectX SDK versions of XAUDIO2 do not take the Flags parameter for <b>GetState</b>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/48b80a66-91c1-973f-069b-6f63422d7154">How to: Stream a Sound from Disk</a>



<a href="https://msdn.microsoft.com/library/Ee415914(v=VS.85).aspx">IXAudio2SourceVoice</a>
 

 

