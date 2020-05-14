---
UID: NF:processthreadsapi.SetProcessInformation
title: SetProcessInformation function (processthreadsapi.h)
description: Sets information for the specified process.
helpviewer_keywords: ["SetProcessInformation","SetProcessInformation function","base.setprocessinformation","processthreadsapi/SetProcessInformation"]
old-location: base\setprocessinformation.htm
tech.root: ProcThread
ms.assetid: 1739fadf-6b43-4b89-8a17-87d9867d5197
ms.date: 12/05/2018
ms.keywords: SetProcessInformation, SetProcessInformation function, base.setprocessinformation, processthreadsapi/SetProcessInformation
f1_keywords:
- processthreadsapi/SetProcessInformation
dev_langs:
- c++
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
api_name:
- SetProcessInformation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetProcessInformation function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Sets information for the specified process.


## -parameters




### -param hProcess [in]

A handle to the process. This handle must have the <b>PROCESS_SET_INFORMATION</b> access 
      right. For more information, see 
      <a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.


### -param ProcessInformationClass [in]

A member of the [PROCESS_INFORMATION_CLASS](/windows/win32/api/processthreadsapi/ne-processthreadsapi-process_information_class) enumeration specifying the kind of information to set.  


### -param ProcessInformation

Pointer to an object that contains the type of information specified by the 
       <i>ProcessInformationClass</i> parameter.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessMemoryPriority</b>, this parameter must point to a 
       <a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-memory_priority_information">MEMORY_PRIORITY_INFORMATION</a> structure.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessPowerThrottling</b>, this parameter must point to a 
       <a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_power_throttling_state">PROCESS_POWER_THROTTLING_STATE</a> structure.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessLeapSecondInfo</b>, this parameter must point to a 
       <a href="https://msdn.microsoft.com/en-us/library/Mt829716(v=VS.85).aspx">PROCESS_LEAP_SECOND_INFO</a> structure.


### -param ProcessInformationSize [in]

The size in bytes of the structure specified by the <i>ProcessInformation</i> parameter.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessMemoryPriority</b>, this parameter must be 
       <code>sizeof(MEMORY_PRIORITY_INFORMATION)</code>.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessPowerThrottling</b>, this parameter must be 
       <code>sizeof(Process_POWER_THROTTLING_STATE)</code>.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessLeapSecondInfo</b>, this parameter must be 
       <code>sizeof(PROCESS_LEAP_SECOND_INFO)</code>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



To help improve system performance, applications should use the 
    <b>SetProcessInformation</b> function with 
    <b>ProcessMemoryPriority</b> to lower the default memory priority of threads that perform 
    background operations or access files and data that are not expected to be accessed again soon. For example, a 
    file indexing application might set a lower default priority for the process that performs the indexing task.

Memory priority helps to determine how long pages remain in the 
    <a href="https://docs.microsoft.com/windows/desktop/Memory/working-set">working set</a> of a process before they are trimmed. A process's 
    memory priority determines the default priority of the physical pages that are added to the process working set by 
    the threads of that process. When the memory manager trims the working set, it trims lower priority pages before 
    higher priority pages. This improves overall system performance because higher priority pages are less likely to 
    be trimmed from the working set and then trigger a page fault when they are accessed again. 


#### Examples

The following example shows how to call 
     <b>SetProcessInformation</b> with 
     <b>ProcessMemoryPriority</b> to set low memory priority as the default for the calling 
     process.

<pre class="syntax" xml:space="preserve"><code>    DWORD ErrorCode;
    BOOL Success;
    MEMORY_PRIORITY_INFORMATION MemPrio;

    //
    // Set low memory priority on the current process.
    //

    ZeroMemory(&amp;MemPrio, sizeof(MemPrio));
    MemPrio.MemoryPriority = MEMORY_PRIORITY_LOW;

    Success = SetProcessInformation(GetCurrentProcess(),
                                   ProcessMemoryPriority,
                                   &amp;MemPrio,
                                   sizeof(MemPrio));

    if (!Success) {
        ErrorCode = GetLastError();
        fprintf(stderr, "Set process memory priority failed: %d\n", ErrorCode);
        goto cleanup;
    }</code></pre>
The following example shows how to call 
     <b>SetProcessInformation</b> with 
     <b>ProcessPowerThrottling</b> to enable throttling policies on a process. 

<pre class="syntax" xml:space="preserve"><code>PROCESS_POWER_THROTTLING_STATE PowerThrottling;
RtlZeroMemory(&amp;PowerThrottling, sizeof(PowerThrottling));
PowerThrottling.Version = PROCESS_POWER_THROTTLING_CURRENT_VERSION;

//
// Turn ExecutionSpeed throttling on. ControlMask selects the mechanism and
// StateMask declares which mechanism should be on or off.
//

PowerThrottling.ControlMask = PROCESS_POWER_THROTTLING_EXECUTION_SPEED;
PowerThrottling.StateMask = PROCESS_POWER_THROTTLING_EXECUTION_SPEED;

SetProcessInformation(GetCurrentProcess(), 
                      ProcessPowerThrottling, 
                      &amp;PowerThrottling, 
                      sizeof(PowerThrottling));

//
// Turn ExecutionSpeed throttling off. ControlMask selects the mechanism and
// StateMask is set to zero as mechanisms should be turned off.
//

PowerThrottling.ControlMask = PROCESS_POWER_THROTTLING_EXECUTION_SPEED;
PowerThrottling.StateMask = 0;

SetProcessInformation(GetCurrentProcess(), 
                      ProcessPowerThrottling, 
                      &amp;PowerThrottling, 
                      sizeof(PowerThrottling));

//
// Let system manage all power throttling. ControlMask is set to 0 as we don’t want // to control any mechanisms.
//

PowerThrottling.ControlMask = 0;
PowerThrottling.StateMask = 0;

SetProcessInformation(GetCurrentProcess(), 
                      ProcessPowerThrottling, 
                      &amp;PowerThrottling, 
                      sizeof(PowerThrottling));
 </code></pre>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getprocessinformation">GetProcessInformation</a>



<a href="/windows/win32/api/processthreadsapi/ns-processthreadsapi-memory_priority_information">MEMORY_PRIORITY_INFORMATION</a>



<a href="https://docs.microsoft.com/previous-versions/mt767996(v=vs.85)">PROCESS_INFORMATION_CLASS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation">SetThreadInformation</a>
 

 

