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

# RefreshPolicyEx function


## -description


The
    <b>RefreshPolicyEx</b> function causes policy to be applied immediately on the computer. The extended function allows you to specify the type of policy refresh to apply.


## -parameters




### -param bMachine [in]

Specifies whether to refresh the computer policy or user policy. If this value is <b>TRUE</b>, the system refreshes the computer policy. If this value is <b>FALSE</b>, the system refreshes the user policy.


### -param dwOptions [in]

Specifies the type of policy refresh to apply. This parameter can be the following value.



#### RP_FORCE

Reapply all policies even if no policy change was detected.

Note that if there are any client-side extensions that can be applied at boot or logon time, (for example, an application installation extension), the extensions are re-applied at the next boot or logon, even if no policy change is detected.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If you do not need to specify the <i>dwOptions</i> parameter, you can call the 
<a href="https://msdn.microsoft.com/e08cb006-d174-4506-87f0-580660bd4023">RefreshPolicy</a> function instead.

By default, policy is reapplied every 90 minutes.




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/f639c11c-ee65-45b6-ba0d-f39c825b3d80">ProcessGroupPolicy</a>



<a href="https://msdn.microsoft.com/df77fece-6e81-4a85-847a-fef3ba775e93">ProcessGroupPolicyEx</a>



<a href="https://msdn.microsoft.com/e08cb006-d174-4506-87f0-580660bd4023">RefreshPolicy</a>
 

 

