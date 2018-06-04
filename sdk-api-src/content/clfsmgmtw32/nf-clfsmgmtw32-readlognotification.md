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

# ReadLogNotification function


## -description


The <b>ReadLogNotification</b> function retrieves notifications from the log manager. It retrieves a queued notification from the log manager immediately if a notification is available; otherwise the request remains pending until a notification is generated.  


## -parameters




### -param hLog [in]

The handle to the log. 


### -param pNotification [out]

Receives the notification type, and if the type has parameters associated with it, the parameters. 


### -param lpOverlapped [in]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that is required for asynchronous operation. If asynchronous operation is not used, this parameter can be <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following is a possible error code:




## -remarks



If the log handle is not created with the <b>FILE_FLAG_OVERLAPPED</b> file option, no operations can start on the log handle while the call to <b>ReadLogNotification</b>  is pending.




## -see-also




<a href="https://msdn.microsoft.com/ba7f7414-885f-40d0-ab61-2348d7f6125b">CLFS_MGMT_NOTIFICATION</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 

