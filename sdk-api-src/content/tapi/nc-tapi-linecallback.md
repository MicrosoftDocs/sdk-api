---
UID: NC:tapi.LINECALLBACK
title: LINECALLBACK
author: windows-sdk-content
description: The lineCallback function is a placeholder for the application-supplied function name.
old-location: tapi2\linecallbackfunc.htm
tech.root: tapi
ms.assetid: 449ecf4f-0b1b-449e-9eae-049770d41dbc
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: LINECALLBACK, LINECALLBACK callback function [TAPI 2.2], _tapi2_linecallbackfunc, lineCallback callback, tapi/LINECALLBACK, tapi2.linecallbackfunc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: tapi.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tapi.h
api_name:
 - LINECALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LINECALLBACK callback function


## -description


The 
<b>lineCallback</b> function is a placeholder for the application-supplied function name.


## -parameters




### -param hDevice

Handle to either a line device or a call associated with the callback. The nature of this handle (line handle or call handle) can be determined by the context provided by <i>dwMsg</i>. Applications must use the <b>DWORD</b> type for this parameter because using the <b>HANDLE</b> type may generate an error.


### -param dwMessage


### -param dwInstance


### -param dwParam1

Parameter for the message.


### -param dwParam2

Parameter for the message.


### -param dwParam3

Parameter for the message.


#### - dwCallbackInstance

Callback instance data passed back to the application in the callback. This <b>DWORD</b> is not interpreted by TAPI.


#### - dwMsg

Line or call device message.


## -returns



This callback function does not return a value.




## -remarks



For information about parameter values passed to this function, see 
<a href="https://msdn.microsoft.com/dc11134e-6c20-426e-834e-508bf855e5da">Line Device Messages</a>.

All callbacks occur in the application's context. The callback function must reside in a DLL or application module.



