---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IXAudio2SourceVoice::GetState


## -description


Returns the voice's current cursor position data.


## -parameters




### -param pVoiceState


Pointer to an <a href="https://msdn.microsoft.com/cb621da1-9d2b-417d-8f7b-661e2efc92f7">XAUDIO2_VOICE_STATE</a> structure containing the state of the voice.


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



<a href="https://msdn.microsoft.com/116DD0E0-8F0B-4934-A48D-FDBE0D0DF049">IXAudio2SourceVoice</a>
 

 

