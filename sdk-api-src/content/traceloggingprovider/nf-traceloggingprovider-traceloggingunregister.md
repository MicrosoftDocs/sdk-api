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

# TraceLoggingUnregister function


## -description


Unregisters a TraceLogging provider.


## -parameters




### -param hProvider [in, out]

A handle to the provider to unregister.


## -returns



This function does not return a value.




## -remarks



You must unregister your provider before it is unloaded or deleted. Otherwise, the ETW callback routines will fail and have unpredictable results.

In regards to thread safety, do not overlap calls to <a href="https://msdn.microsoft.com/621A7DA3-8E75-431C-B747-FFCE72EB2110">TraceLoggingRegister</a>
and <b>TraceLoggingUnregister</b> with calls to other TraceLogging APIs using the
same provider handle. In particular, the call to <b>TraceLoggingRegister</b> must
return before you call <a href="https://msdn.microsoft.com/BFBC6802-64DC-478E-B09D-F550135994AB">TraceLoggingWrite</a> or <b>TraceLoggingUnregister</b>. Calls
to other APIs must also complete before you call <b>TraceLoggingUnregister</b>.

In
addition, you must not call <b>TraceLoggingRegister</b> on a handle that is already
registered or for a handle that could be in the process of being registered or unregistered on another thread.



