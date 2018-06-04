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

# capFileGetCaptureFile macro


## -description



The <b>capFileGetCaptureFile</b> macro returns the name of the current capture file. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/86ce2904-834d-449f-9ef8-5a158c55bbaa">WM_CAP_FILE_GET_CAPTURE_FILE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szName

Pointer to an application-defined buffer used to return the name of the capture file as a null-terminated string. 


### -param wSize

Size, in bytes, of the application-defined buffer referenced by <i>szName</i>. 


## -remarks



The default capture filename is C:\CAPTURE.AVI.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

