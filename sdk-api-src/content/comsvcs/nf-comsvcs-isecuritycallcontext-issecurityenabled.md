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

# ISecurityCallContext::IsSecurityEnabled


## -description


Determines whether security is enabled for the object.


## -parameters




### -param pfIsEnabled [out]

<b>TRUE</b> if the application uses role-based security and role checking is currently enabled for the object; otherwise, <b>FALSE</b>.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



COM+ applications can use one of two types of security: role-based security or process access permissions. If role-based security is being used by the application but is currently disabled, either at the application or component level, <i>pfIsEnabled</i> is  <b>FALSE</b>. Similarly, if the COM+ application uses process access permissions instead of role-based security, <i>pfIsEnabled</i> is <b>FALSE</b>.

You can use this method to find out whether role-based security is enabled before you check role membership using <a href="https://msdn.microsoft.com/544deb46-6427-4936-97a6-ea995b5e77ba">IsCallerInRole</a>. The reason for doing this is that <b>IsCallerInRole</b> is <b>TRUE</b> when role-based security is not enabled. 





## -see-also




<a href="https://msdn.microsoft.com/cd96ef31-784f-40fa-beb5-92a88823326b">ISecurityCallContext</a>



<a href="https://msdn.microsoft.com/6117970c-5dbd-485e-978e-3aa96e42b359">Programmatic Component Security</a>



<a href="https://msdn.microsoft.com/7247758e-f486-4ce2-afca-f0d10fffe626">Role-Based Security</a>
 

 

