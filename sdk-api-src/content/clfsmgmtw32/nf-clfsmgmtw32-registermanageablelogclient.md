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

# RegisterManageableLogClient function


## -description


The <b>RegisterManageableLogClient</b> function registers a client with the log manager. A client can specify whether to receive notifications by using callbacks, or have the notifications  queued for retrieval by using <a href="https://msdn.microsoft.com/08931011-511b-471b-9a4a-ebc96e963c51">ReadLogNotification</a>.


## -parameters




### -param hLog [in]

The handle to the log to register. Only one registration per unique opening of the log is allowed.


### -param pCallbacks [in]

Specifies the callbacks that the client is registering for.  Valid callbacks are enumerated by <a href="https://msdn.microsoft.com/69c657e7-97f0-468a-b349-9891a771c1ed">LOG_MANAGEMENT_CALLBACKS</a>. Specify zero to queue notifications instead.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A client can deregister either by closing the log handle, or by calling <a href="https://msdn.microsoft.com/293a4856-62d4-49a3-9177-4d09a0897200">DeregisterManageableLogClient</a>.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/70d1f73b-bb39-46f8-a2fa-e68693a56082">Creating a Log File</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/293a4856-62d4-49a3-9177-4d09a0897200">DeregisterManageableLogClient</a>



<a href="https://msdn.microsoft.com/69c657e7-97f0-468a-b349-9891a771c1ed">LOG_MANAGEMENT_CALLBACKS</a>
 

 

