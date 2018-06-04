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

# PLOG_UNPINNED_CALLBACK callback function


## -description


The 
<b>LOG_UNPINNED_CALLBACK</b> function is an application-defined callback function that receives notification that the log has become unpinned. The callback is invoked in the context of an asynchronous procedure call (APC)  on the thread that registers for log management.


## -parameters




### -param hLogFile [in]

The handle to the log.


### -param pvClientContext [in]

A pointer to the client context. This is the same context specified when registering the client, which is a member of <a href="https://msdn.microsoft.com/69c657e7-97f0-468a-b349-9891a771c1ed">LOG_MANAGEMENT_CALLBACKS</a>.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/7b8d3b94-2b2e-427e-9b89-530310ecc6fe">LOG_FULL_HANDLER_CALLBACK</a>
 

 

