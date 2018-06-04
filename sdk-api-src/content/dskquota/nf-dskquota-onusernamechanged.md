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

# OnUserNameChanged function


## -description


Occurs when the name information for a <a href="https://msdn.microsoft.com/0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf">DIDiskQuotaUser</a> object has been resolved.


## -parameters




### -param pUser

TBD




#### - oUser

The <b>Object</b> that evaluates to the <a href="https://msdn.microsoft.com/0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf">DIDiskQuotaUser</a> object associated with the user whose name has been resolved.


## -returns



This function does not return a value.




## -remarks



When a client <a href="https://msdn.microsoft.com/0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf">enumerates users</a>, or calls the <a href="https://msdn.microsoft.com/de20d016-83da-42ac-962f-86faf9b25419">AddUser</a> or <a href="https://msdn.microsoft.com/e5767d28-4c0a-49bc-a1d3-ba809411456d">FindUser</a> method, the user name must be resolved to the associated security ID (SID). Because this procedure can be time-consuming, a client can have name resolution done asynchronously on a background thread. When a user's name is resolved, the <a href="https://msdn.microsoft.com/846297f2-b826-45de-8617-228790e87a63">DiskQuotaControl</a> object notifies its client by firing the 
				<b>OnUserNameChanged</b> event. A <b>DIDiskQuotaUser</b> object associated with the user is passed as a parameter. This object allows the client to modify the user's quota settings.




## -see-also




<a href="https://msdn.microsoft.com/846297f2-b826-45de-8617-228790e87a63">DiskQuotaControl Object</a>
 

 

