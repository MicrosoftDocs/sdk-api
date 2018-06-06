---
UID: NF:traceloggingprovider.TraceLoggingRegisterEx
title: TraceLoggingRegisterEx function
author: windows-sdk-content
description: Registers a TraceLogging provider with callback so that it can be used for to log events.
old-location: tracelogging\traceloggingregisterex.htm
old-project: tracelogging
ms.assetid: E64B3855-A43B-489B-8A73-930D65FA5F79
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: TraceLoggingRegisterEx, TraceLoggingRegisterEx function, tracelogging.traceloggingregisterex, traceloggingprovider/TraceLoggingRegisterEx
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
 - TraceLoggingRegisterEx
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: N/A
req.irql: 
req.product: Windows XP with SP1 and later
---

# TraceLoggingRegisterEx function


## -description


Registers a TraceLogging provider with callback so that it can be used for to log events.


## -parameters




### -param hProvider [in, out]

The handle of the provider to register.


### -param pEnableCallback [in, optional]

Callback that ETW calls to notify you when a session enables or disables your provider. Defaults to <b>NULL</b>.


### -param pCallbackContext [in, optional]

Provider-defined context data to pass to the callback when the provider is enabled or disabled. Defaults to <b>NULL</b>.


## -returns



If you call this function from user mode code, the function returns a HRESULT. Use the SUCCEEDED() macro to determine if the function succeeds.

 If you call this function from kernel mode code, the function returns a NTSTATUS. Use the NT_SUCCESS() macro to determine if the function succeeds.




## -remarks



Call this function to register your provider. You need to register before you can use it. If you attempt to register a provider that is already registered, the registration will fail. You can unregister a handler and the register it again if necessary. If registration does fail, all write and unregister commands will have no effect.

Use the SUCCEEDED macro to see if registration was successful.

This function will return an error on versions of Windows that do not support the Event Tracing for Windows (ETW) API, e.g. <a href="https://msdn.microsoft.com/e8b408ba-4bb5-4166-bf43-d18e4fe8de32">EventSetInformation</a>.



