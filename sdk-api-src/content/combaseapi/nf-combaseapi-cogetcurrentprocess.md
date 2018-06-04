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

# CoGetCurrentProcess function


## -description


Returns a value that is unique to the current thread. <b>CoGetCurrentProcess</b> can be used to avoid thread ID reuse problems.


## -parameters






## -returns



The function returns the unique identifier of the current thread.




## -remarks



Using the value returned from a call to <b>CoGetCurrentProcess</b> can help you in maintaining tables that are keyed by threads or in uniquely identifying a thread to other threads or processes.

<b>CoGetCurrentProcess</b> returns a value that is effectively unique, because it is not used again until 2³² more threads have been created on the current workstation or until the workstation is restarted.

The value returned by <b>CoGetCurrentProcess</b> will uniquely identify the same thread for the life of the caller. Because thread IDs can be reused without notice as threads are created and destroyed, this value is more reliable than the value returned by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff546542">GetCurrentThreadId</a> function. 




