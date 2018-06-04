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

# FXECHO_PARAMETERS structure


## -description


Parameters for use with the <a href="https://msdn.microsoft.com/762062de-4e19-5e42-8059-e2f8741bd362">FXECHO XAPOFX</a>.


## -struct-fields




### -field WetDryMix

Ratio of wet (processed) signal to dry (original) signal.


### -field Feedback

Amount of output to feed back into input.


### -field Delay

Delay to all channels in milliseconds. This value must be between <b>FXECHO_MIN_DELAY</b> and <a href="https://msdn.microsoft.com/3bbb0a77-7d42-4823-a5f4-bda7af5eaa2c">FXECHO_INITDATA</a>.<b>MaxDelay</b>.


## -remarks



Echo only supports FLOAT32 audio formats.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

