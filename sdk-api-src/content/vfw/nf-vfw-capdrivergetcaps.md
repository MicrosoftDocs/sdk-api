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

# capDriverGetCaps macro


## -description



The <b>capDriverGetCaps</b> macro returns the hardware capabilities of the capture driver currently connected to a capture window. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/898a800c-1109-47cd-bcc9-cb61d86a4a2e">WM_CAP_DRIVER_GET_CAPS</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

TBD


### -param wSize

Size, in bytes, of the structure referenced by <i>psCaps</i>. 


#### - psCaps

Pointer to the <a href="https://msdn.microsoft.com/6d341be9-6b10-495b-803b-059ead1114cc">CAPDRIVERCAPS</a> structure to contain the hardware capabilities. 


## -remarks



The capabilities returned in <a href="https://msdn.microsoft.com/6d341be9-6b10-495b-803b-059ead1114cc">CAPDRIVERCAPS</a> are constant for a given capture driver. Applications need to retrieve this information once when the capture driver is first connected to a capture window.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

