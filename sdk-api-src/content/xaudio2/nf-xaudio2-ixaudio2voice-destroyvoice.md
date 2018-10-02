---
UID: NF:xaudio2.IXAudio2Voice.DestroyVoice
title: IXAudio2Voice::DestroyVoice
author: windows-sdk-content
description: Destroys the voice. If necessary, stops the voice and removes it from the XAudio2 graph.
old-location: xaudio2\ixaudio2voice_interface_destroyvoice.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2voice.IXAudio2Voice.DestroyVoice
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DestroyVoice, DestroyVoice method [XAudio2 Audio Mixing APIs], DestroyVoice method [XAudio2 Audio Mixing APIs],IXAudio2Voice interface, IXAudio2Voice interface [XAudio2 Audio Mixing APIs],DestroyVoice method, IXAudio2Voice.DestroyVoice, IXAudio2Voice::DestroyVoice, xaudio2.ixaudio2voice_interface_destroyvoice, xaudio2/IXAudio2Voice::DestroyVoice
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
 - IXAudio2Voice.DestroyVoice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXAudio2Voice::DestroyVoice


## -description


Destroys the voice. If necessary, stops the voice and removes it from the XAudio2 graph.


## -parameters






## -returns



This method does not return a value.




## -remarks



If any other voice is currently sending audio to this voice, the method fails.



<b>DestroyVoice</b> waits for the audio processing thread to be idle, so it can take a little while (typically no more than a couple of milliseconds). This is necessary to guarantee that the voice will no longer make any callbacks or read any audio data, so the application can safely free up these resources as soon as the call returns.



To avoid title thread interruptions from a blocking <b>DestroyVoice</b> call, the application can destroy voices on a separate non-critical thread, or the application can use voice pooling strategies to reuse voices rather than destroying them. Note that voices can only be reused with audio that has the same data format and the same number of channels the voice was created with. A voice can play audio data with different sample rates than that of the voice by calling <a href="https://msdn.microsoft.com/58D458C3-528B-4696-8A24-2D66B93695C3">IXAudio2SourceVoice::SetFrequencyRatio</a> with an appropriate ratio parameter.



It is invalid to call <b>DestroyVoice</b> from within a callback (that is, <a href="https://msdn.microsoft.com/D71C117F-826F-41E9-98F4-C6024B3C5103">IXAudio2EngineCallback</a> or <a href="https://msdn.microsoft.com/FF78727D-16AE-40CB-BDE0-664687914FC0">IXAudio2VoiceCallback</a>).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/F704008E-AE43-4189-8B34-8E3915338627">IXAudio2Voice</a>
 

 

