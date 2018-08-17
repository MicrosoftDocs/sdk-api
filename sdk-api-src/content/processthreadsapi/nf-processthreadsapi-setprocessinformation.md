---
UID: NF:processthreadsapi.SetProcessInformation
title: SetProcessInformation function
author: windows-sdk-content
description: Sets information for the specified process.
old-location: base\setprocessinformation.htm
old-project: procthread
ms.assetid: 1739fadf-6b43-4b89-8a17-87d9867d5197
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: SetProcessInformation, SetProcessInformation function, base.setprocessinformation, processthreadsapi/SetProcessInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: PROCESS_MEMORY_EXHAUSTION_TYPE, *PPROCESS_MEMORY_EXHAUSTION_TYPE
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# SetProcessInformation function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Sets information for the specified process.


## -parameters




### -param hProcess [in]

A handle to the process. This handle must have the <b>PROCESS_SET_INFORMATION</b> access 
      right. For more information, see 
      <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param ProcessInformationClass [in]

The class of information to set.  


### -param ProcessInformation

Pointer to an object that contains the type of information specified by the 
       <i>ProcessInformationClass</i> parameter.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessMemoryPriority</b>, this parameter must point to a 
       <a href="https://msdn.microsoft.com/03cacfdf-5c66-42e4-bfcf-afaacd3ad038">MEMORY_PRIORITY_INFORMATION</a> structure.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessPowerThrottling</b>, this parameter must point to a 
       <a href="https://msdn.microsoft.com/394B6509-849C-4B4C-9A46-AF5011A03585">PROCESS_POWER_THROTTLING_STATE</a> structure.

If the <i>ProcessInformationClass</i> parameter is 
       <b>ProcessLeapSecondInfo</b>, this parameter must point to a 
       <a href="base.process_leap_second_info">PROCESS_LEAP_SECOND_INFO</a> structure.


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
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To help improve system performance, applications should use the 
    <b>SetProcessInformation</b> function with 
    <b>ProcessMemoryPriority</b> to lower the default memory priority of threads that perform 
    background operations or access files and data that are not expected to be accessed again soon. For example, a 
    file indexing application might set a lower default priority for the process that performs the indexing task.

Memory priority helps to determine how long pages remain in the 
    <a href="https://msdn.microsoft.com/ff05276a-1d40-4844-b649-10e32e3f1937">working set</a> of a process before they are trimmed. A process's 
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




<a href="https://msdn.microsoft.com/2b075405-b7b6-4da0-b78d-45eaa9c6c8cd">GetProcessInformation</a>



<a href="https://msdn.microsoft.com/03cacfdf-5c66-42e4-bfcf-afaacd3ad038">MEMORY_PRIORITY_INFORMATION</a>



<a href="https://msdn.microsoft.com/4A09E341-82FB-4E50-B2DD-EEDE443F3F1E">PROCESS_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/1739fadf-6b43-4b89-8a17-87d9867d5197">SetThreadInformation</a>
 

 

