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

# capDriverGetVersion macro


## -description



The <b>capDriverGetVersion</b> macro returns the version information of the capture driver connected to a capture window. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/762ebe7e-0d09-46ea-ab17-86061f0bd8f9">WM_CAP_DRIVER_GET_VERSION</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szVer

Pointer to an application-defined buffer used to return the version information as a null-terminated string. 


### -param wSize

Size, in bytes, of the application-defined buffer referenced by <i>szVer</i>. 


## -remarks



The version information is a text string retrieved from the driver's resource area. Applications should allocate approximately 40 bytes for this string. If version information is not available, a <b>NULL</b> string is returned.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

