---
UID: NS:xaudio2.XAUDIO2_VOICE_DETAILS
title: XAUDIO2_VOICE_DETAILS
author: windows-sdk-content
description: Contains information about the creation flags, input channels, and sample rate of a voice.
old-location: xaudio2\xaudio2_voice_details.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_VOICE_DETAILS
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: XAUDIO2_VOICE_DETAILS, XAUDIO2_VOICE_DETAILS structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_voice_details, xaudio2/XAUDIO2_VOICE_DETAILS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
 - HeaderDef
api_location:
 - xaudio2.h
api_name:
 - XAUDIO2_VOICE_DETAILS
product: Windows
targetos: Windows
req.typenames: XAUDIO2_VOICE_DETAILS
req.redist: 
---

# XAUDIO2_VOICE_DETAILS structure


## -description


Contains information about the creation flags, input channels, and sample rate of a voice.


## -struct-fields




### -field CreationFlags

Flags used to create the voice; see the individual voice <a href="https://msdn.microsoft.com/96691e00-9ed0-b31c-fbe9-4daaba0daf98">interfaces</a> for more information.


### -field ActiveFlags

Flags that are currently set on the voice.


### -field InputChannels

The number of input channels the voice expects.


### -field InputSampleRate

The input sample rate the voice expects.


## -remarks



Note the DirectX SDK versions of XAUDIO2 do not support the <b>ActiveFlags</b> member.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c">Structures</a>
 

 

