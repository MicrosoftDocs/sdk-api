---
UID: NF:winbase.SetProcessAffinityMask
title: SetProcessAffinityMask function (winbase.h)
author: windows-sdk-content
description: Sets a processor affinity mask for the threads of the specified process.
old-location: base\setprocessaffinitymask.htm
tech.root: ProcThread
ms.assetid: 210b4c95-4072-4039-aa4f-6b0d85758359
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetProcessAffinityMask, SetProcessAffinityMask function, _win32_setprocessaffinitymask, base.setprocessaffinitymask, winbase/SetProcessAffinityMask
ms.topic: function
f1_keywords: ["winbase/SetProcessAffinityMask"]
req.header: winbase.h
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
 - API-MS-Win-Core-ProcessTopology-Obsolete-l1-1-0.dll
 - API-MS-Win-Core-ProcessTopology-Obsolete-L1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - SetProcessAffinityMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetProcessAffinityMask function


## -description


Sets a processor affinity mask for the threads of the specified process.


## -parameters




### -param hProcess [in]

A handle to the process whose affinity mask is to be set. This handle must have the <b>PROCESS_SET_INFORMATION</b> access right. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.


### -param dwProcessAffinityMask [in]

The affinity mask for the threads of the process.

On a system with more than 64 processors, the affinity mask must specify processors in a single <a href="https://docs.microsoft.com/windows/desktop/ProcThread/processor-groups">processor group</a>. 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the process affinity mask requests a processor that is not configured in the system, the last error code is <b>ERROR_INVALID_PARAMETER</b>.

On a system with more than 64 processors, if the calling process contains threads in more than one processor group, the last error code is <b>ERROR_INVALID_PARAMETER</b>.




## -remarks



A process affinity mask is a bit vector in which each bit represents a logical processor on which the threads of the process are allowed to run. The value of the process affinity mask must be a subset of the system affinity mask values obtained by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask">GetProcessAffinityMask</a> function. A process is only allowed to run on the processors configured into a system. Therefore, the process affinity mask cannot specify a 1 bit for a processor when the system affinity mask specifies a 0 bit for that processor.

Process affinity is inherited by any child process or newly instantiated local process.

Do not call <b>SetProcessAffinityMask</b> in a DLL that may be called by processes other than your own.

On a system with more than 64 processors, the <b>SetProcessAffinityMask</b> function can be used to set the process affinity mask only for processes with threads in a single <a href="https://docs.microsoft.com/windows/desktop/ProcThread/processor-groups">processor group</a>. Use the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask">SetThreadAffinityMask</a> function to set the affinity mask for individual threads in multiple groups. This effectively changes the group assignment of the process.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getprocessaffinitymask">GetProcessAffinityMask</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/multiple-processors">Multiple Processors</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/child-processes">Processes</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/processor-groups">Processor Groups</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setthreadaffinitymask">SetThreadAffinityMask</a>
 

 

