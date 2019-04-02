---
UID: NS:audioclient.AudioClientProperties~r1
title: AudioClientProperties
ms.date: 01/30/19
ms.keywords: AudioClientProperties
ms.topic: language-reference
targetos: Windows
product: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: audioclient.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: AudioClientProperties
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - audioclient.h
api_name:
 - AudioClientProperties
---

# AudioClientProperties structure


## -description


The <b>AudioClientProperties</b> structure is used to set the parameters that describe the properties of the client's audio stream.


## -struct-fields




### -field cbSize

The size of the <b>AudioClientProperties</b> structure, in bytes.


### -field bIsOffload

Boolean value to indicate whether or not the audio stream is hardware-offloaded.


### -field eCategory

An enumeration that is used to specify the category of the audio stream.


### - Options

A member of the <a href="https://msdn.microsoft.com/C9A51FB2-46F5-4F20-B9F2-63EC53CAB3D7">AUDCLNT_STREAMOPTIONS</a> enumeration describing the characteristics of the stream.

Supported in Windows 8.1 and later.


## -remarks



Starting with Windows 10, hardware-offloaded audio streams must be event driven. This means that if you call <a href="https://msdn.microsoft.com/B9B98EF9-C0E1-430A-9C79-1B414F4D67B5">IAudioClient2::SetClientProperties</a> and set the <i>bIsOffload</i> parameter of the <b>AudioClientProperties</b> to TRUE, you must specify the <b>AUDCLNT_STREAMFLAGS_EVENTCALLBACK</b> flag in the <i>StreamFlags</i> parameter to <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>.




## -see-also




<a href="https://msdn.microsoft.com/C9A51FB2-46F5-4F20-B9F2-63EC53CAB3D7">AUDCLNT_STREAMOPTIONS</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh404178(v=VS.85).aspx">AUDIO_STREAM_CATEGORY</a>



<a href="https://msdn.microsoft.com/92585cd4-baa9-4f75-816e-b83f5badad37">Core Audio Structures</a>



<a href="https://msdn.microsoft.com/B9B98EF9-C0E1-430A-9C79-1B414F4D67B5">IAudioClient2::SetClientProperties</a>
 

 

