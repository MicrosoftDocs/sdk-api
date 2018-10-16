---
UID: NF:processthreadsapi.SetThreadInformation
title: SetThreadInformation function
author: windows-sdk-content
description: Sets information for the specified thread.
old-location: base\setthreadinformation.htm
tech.root: procthread
ms.assetid: c0159bea-870a-46b7-a350-91fe52efae49
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: SetThreadInformation, SetThreadInformation function, base.setthreadinformation, processthreadsapi/SetThreadInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: processthreadsapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - SetThreadInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetThreadInformation function


## -description


Sets information for the specified thread. 


## -parameters




### -param hThread [in]

A handle to the thread. The handle must have THREAD_QUERY_INFORMATION access right. For more information, see  <a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.


### -param ThreadInformationClass [in]

The class of information to set. The only supported values are <b>ThreadMemoryPriority</b> and <b>ThreadPowerThrottling</b>.


### -param ThreadInformation

Pointer to a structure that contains the type of information specified by the <i>ThreadInformationClass</i> parameter.

If the <i>ThreadInformationClass</i> parameter is <b>ThreadMemoryPriority</b>, this parameter must point to a <b>MEMORY_PRIORITY_INFORMATION</b> structure.

If the <i>ThreadInformationClass</i> parameter is <b>ThreadPowerThrottling</b>, this parameter must point to a <b>THREAD_POWER_THROTTLING_STATE</b> structure.


### -param ThreadInformationSize [in]

The size in bytes of the structure specified by the <i>ThreadInformation</i> parameter.

If the <i>ThreadInformationClass</i> parameter is <b>ThreadMemoryPriority</b>, this parameter must be <code>sizeof(MEMORY_PRIORITY_INFORMATION)</code>.  

If the <i>ThreadInformationClass</i> parameter is <b>ThreadPowerThrottling</b>, this parameter must be <code>sizeof(THREAD_POWER_THROTTLING_STATE)</code>.  


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To help improve system performance, applications should use the <b>SetThreadInformation</b> function with <b>ThreadMemoryPriority</b> to lower the memory priority of threads that perform background operations or access files and data that are not expected to be accessed again soon. For example, an anti-malware application might lower the priority of threads involved in scanning files. 

Memory priority helps to determine how long pages remain in the <a href="https://msdn.microsoft.com/ff05276a-1d40-4844-b649-10e32e3f1937">working set</a> of a process before they are trimmed. A thread's memory priority determines the minimum priority of the physical pages that are added to the process working set by that thread. When the memory manager trims the working set, it trims lower priority pages before higher priority pages. This improves overall system performance because higher priority pages are less likely to be trimmed from the working set and then trigger a page fault when they are accessed again. 


#### Examples

The following example shows how to call <b>SetThreadInformation</b> with <b>ThreadMemoryPriority</b> to set low memory priority on the current thread.

<pre class="syntax" xml:space="preserve"><code>DWORD ErrorCode;
    BOOL Success;
    MEMORY_PRIORITY_INFORMATION MemPrio;

    //
    // Set low memory priority on the current thread.
    //

    ZeroMemory(&amp;MemPrio, sizeof(MemPrio));
    MemPrio.MemoryPriority = MEMORY_PRIORITY_LOW;

    Success = SetThreadInformation(GetCurrentThread(),
                                   ThreadMemoryPriority,
                                   &amp;MemPrio,
                                   sizeof(MemPrio));

    if (!Success) {
        ErrorCode = GetLastError();
        fprintf(stderr, "Set thread memory priority failed: %d\n", ErrorCode);
        goto cleanup;
    }</code></pre>
The following example shows how to call <b>SetThreadInformation</b> with <b>ThreadPowerThrottling</b> to enable throttling policies on a thread.

<pre class="syntax" xml:space="preserve"><code>THREAD_POWER_THROTTLING_STATE PowerThrottling;
RtlZeroMemory(&amp;PowerThrottling, sizeof(PowerThrottling));
PowerThrottling.Version = THREAD_POWER_THROTTLING_CURRENT_VERSION;

//
// Turn ExecutionSpeed throttling on. ControlMask selects the mechanism and
// StateMask declares which mechanism should be on or off.
//

PowerThrottling.ControlMask = THREAD_POWER_THROTTLING_EXECUTION_SPEED;
PowerThrottling.StateMask = THREAD_POWER_THROTTLING_EXECUTION_SPEED;

SetThreadInformation(GetCurrentThread(), 
                     ThreadPowerThrottling, 
                     &amp;PowerThrottling, 
                     sizeof(PowerThrottling));

//
// Turn ExecutionSpeed throttling off. ControlMask selects the mechanism and
// StateMask is set to zero as mechanisms should be turned off.
//

PowerThrottling.ControlMask = THREAD_POWER_THROTTLING_EXECUTION_SPEED;
PowerThrottling.StateMask = 0;

SetThreadInformation(GetCurrentThread(), 
                     ThreadPowerThrottling, 
                     &amp;PowerThrottling, 
                     sizeof(PowerThrottling));

//
// Let system manage all power throttling. ControlMask is set to 0 as we don’t want // to control any mechanisms.
//

PowerThrottling.ControlMask = 0;
PowerThrottling.StateMask = 0;

SetThreadInformation(GetCurrentThread(), 
                     ThreadPowerThrottling, 
                     &amp;PowerThrottling, 
                     sizeof(PowerThrottling));
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/b7996647-78ab-4f32-bcf6-41aa87d13bb8">GetThreadInformation</a>



<a href="https://msdn.microsoft.com/1739fadf-6b43-4b89-8a17-87d9867d5197">SetProcessInformation</a>
 

 

