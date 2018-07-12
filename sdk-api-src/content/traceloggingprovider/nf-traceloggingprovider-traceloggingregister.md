---
UID: NF:traceloggingprovider.TraceLoggingRegister
title: TraceLoggingRegister function
author: windows-sdk-content
description: Registers a TraceLogging provider so that it can be used for to log events.
old-location: tracelogging\traceloggingregister.htm
old-project: tracelogging
ms.assetid: 621A7DA3-8E75-431C-B747-FFCE72EB2110
ms.author: windowssdkdev
ms.date: 04/27/2018
ms.keywords: TraceLoggingRegister, TraceLoggingRegister function, tracelogging.traceloggingregister, traceloggingprovider/TraceLoggingRegister
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
tech.root: 
req.typenames: TPMVSCMGR_ERROR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - N/A
api_name:
 - TraceLoggingRegister
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: N/A
req.irql: 
req.product: Windows XP with SP1 and later
---

# TraceLoggingRegister function


## -description


Registers a TraceLogging provider so that it can be used for to log events.


## -parameters




### -param hProvider [in, out]

The handle of the provider to register.


## -returns



If you call this function from user mode code, the function returns a HRESULT. Use the SUCCEEDED() macro to determine if the function succeeds.

 If you call this function from kernel mode code, the function returns a NTSTATUS. Use the NT_SUCCESS() macro to determine if the function succeeds.




## -remarks



Call this function to register your provider. You need to register before you can use it. If you attempt to register a provider that is already registered, the results are unpredictable. You can unregister a handler and then register it again if necessary. If registration does fail, all write and unregister commands will have no effect.

Use the SUCCEEDED macro to see if registration was successful.



