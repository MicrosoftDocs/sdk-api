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

# CAPSTATUSCALLBACKA callback function


## -description



The <b>capStatusCallback</b> function is the status callback function used with video capture. The name <b>capStatusCallback</b> is a placeholder for the application-supplied function name.



To set the callback, send the <a href="https://msdn.microsoft.com/451ba9f9-7bfb-4c57-af6c-d5f691f39618">WM_CAP_SET_CALLBACK_STATUS</a> message to the capture window or call the <a href="https://msdn.microsoft.com/7024aa3e-d227-4c22-8259-6299e9205f53">capSetCallbackOnStatus</a> macro.


## -parameters




### -param hWnd

Handle to the capture window associated with the callback function.


### -param nID

Message identification number.


### -param lpsz

Pointer to a textual description of the returned status.


## -remarks



During capture operations, the first message sent to the callback function is always IDS_CAP_BEGIN and the last is always IDS_CAP_END. A message identifier of zero indicates a new operation is starting and the callback function should clear the current status.




## -see-also




<a href="https://msdn.microsoft.com/c93ecc51-e2c5-4b69-8625-c8385d53fab2">Video Capture</a>



<a href="https://msdn.microsoft.com/0fe87fa7-9f07-48f7-958b-da385d9ddaf0">Video Capture Functions</a>
 

 

