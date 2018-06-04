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

# capDriverConnect macro


## -description



The <b>capDriverConnect</b> macro connects a capture window to a capture driver. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/8804bb3c-d06c-4ddc-b116-3d292205a52d">WM_CAP_DRIVER_CONNECT</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param i

TBD






#### - iIndex

Index of the capture driver. The index can range from 0 through 9. 


## -remarks



Connecting a capture driver to a capture window automatically disconnects any previously connected capture driver.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

