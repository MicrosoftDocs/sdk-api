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

# UnregisterSuspendResumeNotification function


## -description


Cancels a registration to receive notification when the system is suspended or resumed. Similar to <a href="https://msdn.microsoft.com/5680e6bd-1694-4d5f-94ea-41b24149c741">PowerUnregisterSuspendResumeNotification</a> but operates in user mode.


## -parameters




### -param Handle

TBD




#### - RegistrationHandle [in, out]

A handle to a registration obtained by calling the <a href="https://msdn.microsoft.com/6cd42d32-07e9-4cbd-83f9-6146b1cb54db">RegisterSuspendResumeNotification</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/6cd42d32-07e9-4cbd-83f9-6146b1cb54db">RegisterSuspendResumeNotification</a>
 

 

