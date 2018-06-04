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

# IXAudio2SourceVoice::SetSourceSampleRate


## -description


Reconfigures the voice to consume source data at a different sample rate than the rate specified when the voice was created.


## -parameters




### -param NewSourceSampleRate [in]

The new sample rate the voice should process submitted data at. Valid sample rates are 1kHz to 200kHz. 


## -returns



Returns S_OK if successful, an error code otherwise. See <a href="https://msdn.microsoft.com/42a1c21c-4b14-114a-d79e-15a61eb2139b">XAudio2 Error Codes</a> for descriptions of error codes.






## -remarks



The <b>SetSourceSampleRate</b> method supports reuse of XAudio2 voices by allowing a voice to play sounds with a variety of sample rates. To use <b>SetSourceSampleRate</b> the voice must have been created without the XAUDIO2_VOICE_NOPITCH or XAUDIO2_VOICE_NOSRC flags and must not have any buffers currently queued.



The typical use of <b>SetSourceSampleRate</b> is to support voice pooling. For example to support voice pooling an application would precreate all the voices it expects to use. Whenever a new sound will be played the application chooses an inactive voice or ,if all voices are busy, picks the least important voice and calls <b>SetSourceSampleRate</b> on the voice with the new sound's sample rate. After <b>SetSourceSampleRate</b> has been called on the voice, the application can immediately start submitting and playing buffers with the new sample rate. This allows the application to avoid the overhead of creating and destroying voices frequently during gameplay.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/116DD0E0-8F0B-4934-A48D-FDBE0D0DF049">IXAudio2SourceVoice</a>
 

 

