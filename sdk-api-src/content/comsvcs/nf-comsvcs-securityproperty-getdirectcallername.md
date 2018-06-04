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

# SecurityProperty::GetDirectCallerName


## -description


Retrieves the user name associated with the external process that called the currently executing method.


## -parameters




### -param bstrUserName [out]

A reference to the user name associated with the external process that called the currently executing method.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



The following scenarios illustrate the functionality of this method:

<ul>
<li>A base process, running on server A as user A, calls into object X on server B, running as user B. Then object X calls into object Y, running on server C. If object Y calls <b>GetDirectCallerName</b>, the name of user B is retrieved.</li>
<li>A base process, running on server A as user A, calls into object X on server B, running as user B. Then object X calls into object Y, running in the same process as object X, also on server B. When object Y calls <b>GetDirectCallerName</b>, the name of user A is returned, not the name of user B.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/e4eb8e83-3510-4c2c-8b9c-563bfcbf48b3">SecurityProperty</a>
 

 

