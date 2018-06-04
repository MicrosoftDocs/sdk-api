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

# capCaptureSetSetup macro


## -description



The <b>capCaptureSetSetup</b> macro sets the configuration parameters used with streaming capture. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/ba9adb26-6627-469b-a836-f4f277ddb7c4">WM_CAP_SET_SEQUENCE_SETUP</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param s

TBD


### -param wSize

Size, in bytes, of the structure referenced by s. 


#### - psCapParms

Pointer to a CAPTUREPARMS structure. 


## -remarks



For information about the parameters used to control streaming capture, see the <a href="https://msdn.microsoft.com/6bf7e374-5991-4a7b-984a-628d3e77b2d7">CAPTUREPARMS</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

