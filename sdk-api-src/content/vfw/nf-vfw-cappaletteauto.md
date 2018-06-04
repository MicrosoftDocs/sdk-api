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

# capPaletteAuto macro


## -description



The <b>capPaletteAuto</b> macro requests that the capture driver sample video frames and automatically create a new palette. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/b94d245d-adf4-4fe0-b053-87109ef5fd2f">WM_CAP_PAL_AUTOCREATE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param iFrames

Number of frames to sample. 


### -param iColors

Number of colors in the palette. The maximum value for this parameter is 256. 


## -remarks



The sampled video sequence should include all the colors you want in the palette. To obtain the best palette, you might have to sample the whole sequence rather than a portion of it.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

