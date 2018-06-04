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



