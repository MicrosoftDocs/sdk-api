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

# DeleteUmsThreadContext function


## -description


Deletes  the specified user-mode scheduling (UMS) thread context. The thread must be terminated. 


## -parameters




### -param UmsThread [in]

A pointer to the UMS thread context to be deleted. The <a href="https://msdn.microsoft.com/b27ce81a-8463-46af-8acf-2de091f625df">CreateUmsThreadContext</a> function provides this pointer.


## -returns



If the function succeeds, it returns a nonzero value.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



A UMS thread context cannot be deleted until the associated thread has terminated. 

When a UMS worker thread finishes running (for example, by returning from its thread entry point function),   the system terminates the thread,  sets the  termination status in the thread's UMS thread context, and queues the UMS thread context to the associated completion list.

 Any attempt to execute the  UMS thread will fail because the thread is already terminated. 

To check the termination status of a thread, the application's scheduler should call <a href="https://msdn.microsoft.com/5f694edf-ba5e-45a2-a938-5013edddcae2">QueryUmsThreadInformation</a> with the <b>UmsIsThreadTerminated</b> information class. 




## -see-also




<a href="https://msdn.microsoft.com/b27ce81a-8463-46af-8acf-2de091f625df">CreateUmsThreadContext</a>



<a href="https://msdn.microsoft.com/5f694edf-ba5e-45a2-a938-5013edddcae2">QueryUmsThreadInformation</a>
 

 

