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

# IAudioProcessingObject::GetInputChannelCount


## -description


GetInputChannelCount returns the input channel count (samples-per-frame) for this APO. 


## -parameters




### -param pu32ChannelCount [out]

The input channel count.


## -returns



<code>GetInputChannelCount</code> returns a value of S_OK if the call was successful.




## -remarks



The input channel count that is returned refers to the input side of the APO.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536501">IAudioProcessingObject</a>
 

 

