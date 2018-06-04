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

# capSetAudioFormat macro


## -description



The <b>capSetAudioFormat</b> macro sets the audio format to use when performing streaming or step capture. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/8bffa401-3d36-43bb-9f69-988ebc69b860">WM_CAP_SET_AUDIOFORMAT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

TBD


### -param wSize

Size, in bytes, of the structure referenced by <i>psAudioFormat</i>. 


#### - psAudioFormat

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> or <a href="https://msdn.microsoft.com/c09dc3f0-e1bc-4643-9b27-bcf1dcc5710c">PCMWAVEFORMAT</a> structure that defines the audio format. 


## -see-also




<a href="https://msdn.microsoft.com/c09dc3f0-e1bc-4643-9b27-bcf1dcc5710c">PCMWAVEFORMAT</a>



<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a>



<a href="https://msdn.microsoft.com/8bffa401-3d36-43bb-9f69-988ebc69b860">WM_CAP_SET_AUDIOFORMAT</a>
 

 

