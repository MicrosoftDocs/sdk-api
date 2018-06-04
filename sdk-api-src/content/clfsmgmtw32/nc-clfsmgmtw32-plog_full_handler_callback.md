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

# PLOG_FULL_HANDLER_CALLBACK callback function


## -description


The 
<b>LOG_FULL_HANDLER_CALLBACK</b> function is an application-defined callback function that receives notification that the call to <a href="https://msdn.microsoft.com/ed4b067f-9386-4bec-a6dc-b22d6fd52390">HandleLogFull</a> is complete. The callback is invoked in the context of an asynchronous procedure call (APC) on the thread that registered for log management.


## -parameters




### -param hLogFile [in]

The handle to the log.


### -param dwError [in]

The status of the operation.


### -param fLogIsPinned [in]

Specifies if the log is considered "pinned". If <i>fLogIsPinned</i> is <b>TRUE</b> and the log is then unpinned, the <a href="https://msdn.microsoft.com/ab3b5ffb-01a5-4678-bcfa-7e71b1f4c0f3">LOG_UNPINNED_CALLBACK</a> is invoked.


### -param pvClientContext [in]

A pointer to the client context.


## -returns



This function does not return a value.




## -remarks



The client application determines which actions this callback function performs.




## -see-also




<a href="https://msdn.microsoft.com/ab3b5ffb-01a5-4678-bcfa-7e71b1f4c0f3">LOG_UNPINNED_CALLBACK</a>
 

 

