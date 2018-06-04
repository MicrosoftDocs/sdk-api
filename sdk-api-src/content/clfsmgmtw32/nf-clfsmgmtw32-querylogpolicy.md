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

# QueryLogPolicy function


## -description


The <b>QueryLogPolicy</b> function allows you to obtain a policy that is installed for the specified log.


## -parameters




### -param hLog [in]

The handle to the log to query.


### -param ePolicyType [in]

Specifies the type of policy to query for. Policy types are enumerated in <a href="https://msdn.microsoft.com/library/windows/hardware/ff541849">CLFS_MGMT_POLICY_TYPE</a>.


### -param pPolicyBuffer [out]

A pointer to a buffer to receive the returned policies.


### -param pcbPolicyBuffer [in, out]

A pointer to the size of <i>pPolicyBuffer</i>. If the buffer is not large enough, <i>pcbPolicyBuffer</i> receives the size buffer required to successfully retrieve the specified policies.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541842">CLFS_MGMT_POLICY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541849">CLFS_MGMT_POLICY_TYPE</a>



<a href="https://msdn.microsoft.com/06e8c1bf-f190-4f3d-a588-5c8dd2e99f43">RemoveLogPolicy</a>
 

 

