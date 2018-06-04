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



