---
UID: NF:traceloggingprovider.TraceLoggingUnregister
title: TraceLoggingUnregister function
author: windows-sdk-content
description: Unregisters a TraceLogging provider.
old-location: tracelogging\traceloggingunregister.htm
old-project: tracelogging
ms.assetid: 4A0217E4-D633-4A6F-B1EE-6A3B2A644DBB
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: TraceLoggingUnregister, TraceLoggingUnregister function, tracelogging.traceloggingunregister, traceloggingprovider/TraceLoggingUnregister
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: traceloggingprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TPMVSCMGR_ERROR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	N/A
api_name:
-	TraceLoggingUnregister
product: Windows
targetos: Windows
req.lib: Advap32.lib
req.dll: N/A
req.irql: 
req.product: Windows XP with SP1 and later
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



