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

# XAUDIO2_VOICE_DETAILS structure


## -description


Contains information about the creation flags, input channels, and sample rate of a voice.


## -struct-fields




### -field CreationFlags

Flags used to create the voice; see the individual voice <a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">interfaces</a> for more information.


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




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

