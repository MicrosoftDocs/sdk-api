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

# capSetVideoFormat macro


## -description



The <b>capSetVideoFormat</b> macro sets the format of captured video data. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/4f9cf90d-7ccb-4fc7-aad5-3d7e082526be">WM_CAP_SET_VIDEOFORMAT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

TBD


### -param wSize

The size, in bytes, of the structure referenced by <i>psVideoFormat</i>. 


#### - psVideoFormat

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure. 


## -remarks



Because video formats are device-specific, applications should check the return value from this function to determine if the format is accepted by the driver.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

