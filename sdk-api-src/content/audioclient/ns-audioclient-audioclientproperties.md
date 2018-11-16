---
UID: NS:audioclient.AudioClientProperties
title: AudioClientProperties
author: windows-sdk-content
description: The AudioClientProperties structure is used to set the parameters that describe the properties of the client's audio stream.
old-location: coreaudio\audioclientproperties.htm
tech.root: CoreAudio
ms.assetid: 5BCCD581-DB66-4939-A62A-2236B9E49AA7
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AudioClientProperties, AudioClientProperties structure [Core Audio], PAudioClientProperties, PAudioClientProperties structure pointer [Core Audio], audioclient/AudioClientProperties, audioclient/PAudioClientProperties, coreaudio.audioclientproperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: audioclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - HeaderDef
api_location:
 - Audioclient.h
api_name:
 - AudioClientProperties
product: Windows
targetos: Windows
req.typenames: AudioClientProperties
req.redist: 
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


#### - Options

A member of the <a href="https://msdn.microsoft.com/C9A51FB2-46F5-4F20-B9F2-63EC53CAB3D7">AUDCLNT_STREAMOPTIONS</a> enumeration describing the characteristics of the stream.

Supported in Windows 8.1 and later.


## -remarks



Starting with Windows 10, hardware-offloaded audio streams must be event driven. This means that if you call <a href="https://msdn.microsoft.com/B9B98EF9-C0E1-430A-9C79-1B414F4D67B5">IAudioClient2::SetClientProperties</a> and set the <i>bIsOffload</i> parameter of the <b>AudioClientProperties</b> to TRUE, you must specify the <b>AUDCLNT_STREAMFLAGS_EVENTCALLBACK</b> flag in the <i>StreamFlags</i> parameter to <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>.




## -see-also




<a href="https://msdn.microsoft.com/C9A51FB2-46F5-4F20-B9F2-63EC53CAB3D7">AUDCLNT_STREAMOPTIONS</a>



<a href="https://msdn.microsoft.com/B6B9195A-2704-4633-AFCF-B01CED6B6DB4">AUDIO_STREAM_CATEGORY</a>



<a href="https://msdn.microsoft.com/92585cd4-baa9-4f75-816e-b83f5badad37">Core Audio Structures</a>



<a href="https://msdn.microsoft.com/B9B98EF9-C0E1-430A-9C79-1B414F4D67B5">IAudioClient2::SetClientProperties</a>
 

 

