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

# XAUDIO2_VOICE_STATE structure


## -description


Returns the voice's current state and cursor position data.


## -struct-fields




### -field pCurrentBufferContext

Pointer to a buffer context provided in the <a href="https://msdn.microsoft.com/b6c2a08b-6abb-4e6a-8acb-6f8983aef95f">XAUDIO2_BUFFER</a> that is processed currently, or, if the voice is stopped currently, to the next buffer due to be processed. <b>pCurrentBufferContext</b> is NULL if there are no buffers in the queue.


### -field BuffersQueued

Number of audio buffers currently queued on the voice, including the one that is processed currently.


### -field SamplesPlayed

Total number of samples processed by this voice since it last started, or since the last audio stream ended (as marked with the XAUDIO2_END_OF_STREAM flag). This total includes samples played multiple times due to looping. Theoretically, if all audio emitted by the voice up to this time is captured, this parameter would be the length of the audio stream in samples. If you specify <b>XAUDIO2_VOICE_NOSAMPLESPLAYED</b> when you call <a href="https://msdn.microsoft.com/6F466C04-D5AD-4B66-A806-9B379582D4DF">IXAudio2SourceVoice::GetState</a>, this member won't be calculated, and its value is unspecified on return from <b>IXAudio2SourceVoice::GetState</b>. <b>IXAudio2SourceVoice::GetState</b> takes about one-third as much time to complete when you specify <b>XAUDIO2_VOICE_NOSAMPLESPLAYED</b>. 


## -remarks



For all encoded formats, including constant bit rate (CBR) formats such as adaptive differential pulse code modulation (ADPCM), <b>SamplesPlayed</b> is expressed in terms of decoded samples. For pulse code modulation (PCM) formats, <b>SamplesPlayed</b> is expressed in terms of either input or output samples. There is a one-to-one mapping from input to output for PCM formats.



If a client needs to get the correlated positions of several voices—that is, to know exactly which sample of a particular voice is playing when a specified sample of another voice is playing—it must make the <a href="https://msdn.microsoft.com/6F466C04-D5AD-4B66-A806-9B379582D4DF">IXAudio2SourceVoice::GetState</a> calls in an XAudio2 engine callback. Doing this ensures that none of the voices advance while the calls are made.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

