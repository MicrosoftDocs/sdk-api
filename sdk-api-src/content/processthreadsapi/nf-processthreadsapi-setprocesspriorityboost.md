---
UID: NF:processthreadsapi.SetProcessPriorityBoost
title: SetProcessPriorityBoost function (processthreadsapi.h)
description: Disables or enables the ability of the system to temporarily boost the priority of the threads of the specified process.
helpviewer_keywords: ["SetProcessPriorityBoost","SetProcessPriorityBoost function","_win32_setprocesspriorityboost","base.setprocesspriorityboost","processthreadsapi/SetProcessPriorityBoost"]
old-location: base\setprocesspriorityboost.htm
tech.root: ProcThread
ms.assetid: 211069cb-4b4c-49bc-ad3c-1be184999670
ms.date: 12/05/2018
ms.keywords: SetProcessPriorityBoost, SetProcessPriorityBoost function, _win32_setprocesspriorityboost, base.setprocesspriorityboost, processthreadsapi/SetProcessPriorityBoost
f1_keywords:
- processthreadsapi/SetProcessPriorityBoost
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetProcessPriorityBoost function


## -description


Disables or enables the ability of the system to temporarily boost the priority of the threads of the specified process.


## -parameters




### -param hProcess [in]

A handle to the process. This handle must have the PROCESS_SET_INFORMATION access right. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.


### -param bDisablePriorityBoost [in]

If this parameter is TRUE, dynamic boosting is disabled. If the parameter is FALSE, dynamic boosting is enabled.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



When a thread is running in one of the dynamic priority classes, the system temporarily boosts the thread's priority when it is taken out of a wait state. If 
<b>SetProcessPriorityBoost</b> is called with the <i>DisablePriorityBoost</i> parameter set to TRUE, its threads' priorities are not boosted. This setting affects all existing threads and any threads subsequently created by the process. To restore normal behavior, call 
<b>SetProcessPriorityBoost</b> with <i>DisablePriorityBoost</i> set to FALSE.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost">GetProcessPriorityBoost</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/priority-boosts">Priority Boosts</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/child-processes">Processes</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/scheduling-priorities">Scheduling Priorities</a>
 

 

