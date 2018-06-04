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

# ReleaseMutex function


## -description


Releases ownership of the specified mutex object.


## -parameters




### -param hMutex [in]

A handle to the mutex object. The 
<a href="https://msdn.microsoft.com/c8315d1c-98c9-4f0a-ae0d-800d7d8100cd">CreateMutex</a> or 
<a href="https://msdn.microsoft.com/0ea363c2-1ff7-4bf5-9e94-f1f17b8c8a11">OpenMutex</a> function returns this handle. 





## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>ReleaseMutex</b> function fails if the calling thread does not own the mutex object.

A thread obtains ownership of a mutex either by creating it with the <i>bInitialOwner</i> parameter set to <b>TRUE</b> or by specifying its handle in a call to one of the 
<a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">wait functions</a>. When the thread no longer needs to own the mutex object, it calls the 
<b>ReleaseMutex</b> function so that another thread can acquire ownership.

A thread  can specify a  mutex that it already owns in a call to one of the wait functions without blocking its execution. This prevents a thread from deadlocking itself while waiting for a mutex that it already owns. However, to release its ownership, the thread must call 
<b>ReleaseMutex</b> one time for each time that it obtained ownership (either through <a href="https://msdn.microsoft.com/c8315d1c-98c9-4f0a-ae0d-800d7d8100cd">CreateMutex</a> or a wait function).


#### Examples

For an example that uses 
<b>ReleaseMutex</b>, see 
<a href="https://msdn.microsoft.com/0f69ba50-69ce-467a-b068-8fd8f07c6c78">Using Mutex Objects</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/c8315d1c-98c9-4f0a-ae0d-800d7d8100cd">CreateMutex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556417">Mutex Objects</a>



<a href="https://msdn.microsoft.com/9b6359c2-0113-49b6-83d0-316ad95aba1b">Synchronization Functions</a>
 

 

