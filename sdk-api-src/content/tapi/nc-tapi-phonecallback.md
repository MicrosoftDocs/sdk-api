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

# PHONECALLBACK callback function


## -description


The 
<b>phoneCallback</b> function is a placeholder for the application-supplied function name.


## -parameters




### -param hDevice

Handle to a phone device associated with the callback.


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



For more information about the parameters passed to this callback function, see 
<a href="https://msdn.microsoft.com/d302819e-c522-470a-be5e-52625c9223a4">TAPI Messages</a>.

All callbacks occur in the application's context. The callback function must reside in a dynamic-link library (DLL) or application module and be exported in the module-definition file.



