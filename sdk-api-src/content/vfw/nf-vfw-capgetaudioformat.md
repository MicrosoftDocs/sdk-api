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

# capGetAudioFormat macro


## -description



The <b>capGetAudioFormat</b> macro obtains the audio format. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/25e58863-2b1e-4ed8-9f34-c39617a15bc1">WM_CAP_GET_AUDIOFORMAT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

TBD


### -param wSize

Size, in bytes, of the structure referenced by <i>s</i>. 


#### - psAudioFormat

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure, or <b>NULL</b>. If the value is <b>NULL</b>, the size, in bytes, required to hold the <b>WAVEFORMATEX</b> structure is returned. 


## -remarks



Because compressed audio formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the audio format data.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

