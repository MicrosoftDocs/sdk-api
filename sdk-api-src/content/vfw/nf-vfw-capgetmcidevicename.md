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

# capGetMCIDeviceName macro


## -description



The <b>capGetMCIDeviceName</b> macro retrieves the name of an MCI device previously set with the <a href="https://msdn.microsoft.com/2dabc360-7f69-4dbb-9826-0657eec265ff">capSetMCIDeviceName</a> macro. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/c5d7d955-ab6a-4959-b79e-9ff35a282ba2">WM_CAP_GET_MCI_DEVICE</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param szName

Pointer to a null-terminated string that contains the MCI device name. 


### -param wSize

Length, in bytes, of the buffer referenced by <i>szName</i> . 


## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

