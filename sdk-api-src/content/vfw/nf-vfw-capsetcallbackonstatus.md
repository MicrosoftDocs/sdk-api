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

# capSetCallbackOnStatus macro


## -description



The <b>capSetCallbackOnStatus</b> macro sets a status callback function in the application. AVICap calls this procedure whenever the capture window status changes. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/451ba9f9-7bfb-4c57-af6c-d5f691f39618">WM_CAP_SET_CALLBACK_STATUS</a> message.




## -parameters




### -param hwnd

Handle to a capture window. 


### -param fpProc

Pointer to the status callback function, of type <a href="https://msdn.microsoft.com/b48021a7-7fa1-4837-a6ca-af266fd55f4f">capStatusCallback</a>. Specify <b>NULL</b> for this parameter to disable a previously installed status callback function. 


## -remarks



Applications can optionally set a status callback function. If set, AVICap calls this procedure in the following situations:

<ul>
<li>A capture session is completed.</li>
<li>A capture driver successfully connected to a capture window.</li>
<li>An optimal palette is created.</li>
<li>The number of captured frames is reported.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/9aa98340-a5a0-4084-9670-b3c27a1351ed">Creating a Status Callback Function</a>



<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/21061f06-d58b-4800-a9f5-9821494fabd6">Video Capture Macros</a>
 

 

