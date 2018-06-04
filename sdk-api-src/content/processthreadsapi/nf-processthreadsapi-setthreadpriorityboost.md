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

# SetThreadPriorityBoost function


## -description


Disables or enables the ability of the system to temporarily boost the priority of a thread.


## -parameters




### -param hThread [in]

A handle to the thread whose priority is to be boosted. The handle must have the <b>THREAD_SET_INFORMATION</b> or <b>THREAD_SET_LIMITED_INFORMATION</b> access right. For more information, see 
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the <b>THREAD_SET_INFORMATION</b> access right.


### -param bDisablePriorityBoost

TBD




#### - DisablePriorityBoost [in]

If this parameter is <b>TRUE</b>, dynamic boosting is disabled. If the parameter is <b>FALSE</b>, dynamic boosting is enabled.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When a thread is running in one of the dynamic priority classes, the system temporarily boosts the thread's priority when it is taken out of a wait state. If 
<b>SetThreadPriorityBoost</b> is called with the <i>DisablePriorityBoost</i> parameter set to <b>TRUE</b>, the thread's priority is not boosted. To restore normal behavior, call 
<b>SetThreadPriorityBoost</b> with <i>DisablePriorityBoost</i> set to <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/44edf5e3-7543-482f-89ff-ae9daf495ff3">GetThreadPriorityBoost</a>



<a href="https://msdn.microsoft.com/d020ecc5-89d1-4a0d-a197-15a66e269e86">OpenThread</a>



<a href="https://msdn.microsoft.com/bcc6cec7-2d85-4810-98d0-7d99486f4924">Priority Boosts</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/8710cd56-6bf3-4317-a1f6-1a159394ce2a">Scheduling Priorities</a>



<a href="https://msdn.microsoft.com/a78c17dc-d5d9-4baf-8770-597b04fa3fa8">Threads</a>
 

 

