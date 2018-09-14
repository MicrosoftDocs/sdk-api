---
UID: NF:processthreadsapi.SetProcessPriorityBoost
title: SetProcessPriorityBoost function
author: windows-sdk-content
description: Disables or enables the ability of the system to temporarily boost the priority of the threads of the specified process.
old-location: base\setprocesspriorityboost.htm
tech.root: procthread
ms.assetid: 211069cb-4b4c-49bc-ad3c-1be184999670
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: SetProcessPriorityBoost, SetProcessPriorityBoost function, _win32_setprocesspriorityboost, base.setprocesspriorityboost, processthreadsapi/SetProcessPriorityBoost
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - SetProcessPriorityBoost
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetProcessPriorityBoost function


## -description


Disables or enables the ability of the system to temporarily boost the priority of the threads of the specified process.


## -parameters




### -param hProcess [in]

A handle to the process. This handle must have the PROCESS_SET_INFORMATION access right. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param bDisablePriorityBoost

TBD




#### - DisablePriorityBoost [in]

If this parameter is TRUE, dynamic boosting is disabled. If the parameter is FALSE, dynamic boosting is enabled.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When a thread is running in one of the dynamic priority classes, the system temporarily boosts the thread's priority when it is taken out of a wait state. If 
<b>SetProcessPriorityBoost</b> is called with the <i>DisablePriorityBoost</i> parameter set to TRUE, its threads' priorities are not boosted. This setting affects all existing threads and any threads subsequently created by the process. To restore normal behavior, call 
<b>SetProcessPriorityBoost</b> with <i>DisablePriorityBoost</i> set to FALSE.




## -see-also




<a href="https://msdn.microsoft.com/b47944f2-b724-4eec-9dcf-2d14a7b77456">GetProcessPriorityBoost</a>



<a href="https://msdn.microsoft.com/bcc6cec7-2d85-4810-98d0-7d99486f4924">Priority Boosts</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/4bdec0f5-7276-422e-9935-0e231b0fc17d">Processes</a>



<a href="https://msdn.microsoft.com/8710cd56-6bf3-4317-a1f6-1a159394ce2a">Scheduling Priorities</a>
 

 

