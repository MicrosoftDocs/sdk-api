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

# CoSuspendClassObjects function


## -description


Prevents any new activation requests from the SCM on all class objects registered within the process.


## -parameters






## -returns



This function returns S_OK to indicate that the activation of class objects was successfully suspended.




## -remarks



<b>CoSuspendClassObjects</b> prevents any new activation requests from the SCM on all class objects registered within the process. Even though a process may call this function, the process still must call the <a href="https://msdn.microsoft.com/90b9b9ca-b5b2-48f5-8c2a-b478b6daa7ec">CoRevokeClassObject</a> function for each CLSID it has registered, in the apartment it registered in. Applications typically do not need to call this function, which is generally only called internally by OLE when used in conjunction with the <a href="https://msdn.microsoft.com/b28d41e2-4144-413d-9963-14f2d4dc8876">CoReleaseServerProcess</a> function.





## -see-also




<a href="https://msdn.microsoft.com/b28d41e2-4144-413d-9963-14f2d4dc8876">CoReleaseServerProcess</a>



<a href="https://msdn.microsoft.com/90b9b9ca-b5b2-48f5-8c2a-b478b6daa7ec">CoRevokeClassObject</a>



<a href="https://msdn.microsoft.com/18641a84-56f8-4d27-9ddb-fa64011ac8ba">Out-of-Process Server Implementation Helpers</a>
 

 

