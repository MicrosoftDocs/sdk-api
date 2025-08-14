---
UID: NF:processthreadsapi.SetThreadInformation
title: SetThreadInformation function (processthreadsapi.h)
description: Sets information for the specified thread.
helpviewer_keywords: ["SetThreadInformation","SetThreadInformation function","base.setthreadinformation","processthreadsapi/SetThreadInformation"]
old-location: base\setthreadinformation.htm
tech.root: processthreadsapi
ms.assetid: c0159bea-870a-46b7-a350-91fe52efae49
ms.date: 12/05/2018
ms.keywords: SetThreadInformation, SetThreadInformation function, base.setthreadinformation, processthreadsapi/SetThreadInformation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetThreadInformation
 - processthreadsapi/SetThreadInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
api_name:
 - SetThreadInformation
---

# SetThreadInformation function


## -description

Sets information for the specified thread.

## -parameters

### -param hThread [in]

A handle to the thread. The handle must have THREAD_SET_INFORMATION access right. For more information, see  <a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

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
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To help improve system performance, applications should use the <b>SetThreadInformation</b> function with <b>ThreadMemoryPriority</b> to lower the memory priority of threads that perform background operations or access files and data that are not expected to be accessed again soon. For example, an anti-malware application might lower the priority of threads involved in scanning files. 

**Memory priority** helps to determine how long pages remain in the <a href="/windows/desktop/Memory/working-set">working set</a> of a process before they are trimmed. A thread's memory priority determines the minimum priority of the physical pages that are added to the process working set by that thread. When the memory manager trims the working set, it trims lower priority pages before higher priority pages. This improves overall system performance because higher priority pages are less likely to be trimmed from the working set and then trigger a page fault when they are accessed again. 

**ThreadPowerThrottling** enables throttling policies on a thread, which can be used to balance out performance and power efficiency in cases where optimal performance is not required. When a thread opts into enabling <code>THREAD_POWER_THROTTLING_EXECUTION_SPEED</code>, the thread will be classified as EcoQoS. The system will try to increase power efficiency through strategies such as reducing CPU frequency or using more power efficient cores. EcoQoS should be used when the work is not contributing to the foreground user experience, which provides longer battery life, and reduced heat and fan noise. EcoQoS should not be used for performance critical or foreground user experiences. (Prior to Windows 11, the EcoQoS level did not exist and the process was instead labeled as LowQoS). If an application does not explicitly enable <code>THREAD_POWER_THROTTLING_EXECUTION_SPEED</code>, the system will use its own heuristics to automatically infer a Quality of Service level. For more information, see <a href="/windows/win32/procthread/quality-of-service">Quality of Service</a>.

#### Examples

The following example shows how to call <b>SetThreadInformation</b> with <b>ThreadMemoryPriority</b> to set low memory priority on the current thread.


```c
DWORD ErrorCode;
BOOL Success;
MEMORY_PRIORITY_INFORMATION MemPrio;

//
// Set low memory priority on the current thread.
//

ZeroMemory(&MemPrio, sizeof(MemPrio));
MemPrio.MemoryPriority = MEMORY_PRIORITY_LOW;

Success = SetThreadInformation(GetCurrentThread(),
                               ThreadMemoryPriority,
                               &MemPrio,
                               sizeof(MemPrio));

if (!Success) {
    ErrorCode = GetLastError();
    fprintf(stderr, "Set thread memory priority failed: %d\n", ErrorCode);
}
```

The following example shows how to call <b>SetThreadInformation</b> with <b>ThreadPowerThrottling</b> to control the Quality of Service of a thread.

```c
THREAD_POWER_THROTTLING_STATE PowerThrottling;
ZeroMemory(&PowerThrottling, sizeof(PowerThrottling));
PowerThrottling.Version = THREAD_POWER_THROTTLING_CURRENT_VERSION;

//
// EcoQoS
// Turn EXECUTION_SPEED throttling on. 
// ControlMask selects the mechanism and StateMask declares which mechanism should be on or off.
//

PowerThrottling.ControlMask = THREAD_POWER_THROTTLING_EXECUTION_SPEED;
PowerThrottling.StateMask = THREAD_POWER_THROTTLING_EXECUTION_SPEED;

SetThreadInformation(GetCurrentThread(), 
                     ThreadPowerThrottling, 
                     &PowerThrottling, 
                     sizeof(PowerThrottling));

//
// HighQoS
// Turn EXECUTION_SPEED throttling off.
// ControlMask selects the mechanism and StateMask is set to zero as mechanisms should be turned off.
//

PowerThrottling.ControlMask = THREAD_POWER_THROTTLING_EXECUTION_SPEED;
PowerThrottling.StateMask = 0;

SetThreadInformation(GetCurrentThread(), 
                     ThreadPowerThrottling, 
                     &PowerThrottling, 
                     sizeof(PowerThrottling));

//
// Let system manage all power throttling. ControlMask is set to 0 as we don’t want 
// to control any mechanisms.
//

PowerThrottling.ControlMask = 0;
PowerThrottling.StateMask = 0;

SetThreadInformation(GetCurrentThread(), 
                     ThreadPowerThrottling, 
                     &PowerThrottling, 
                     sizeof(PowerThrottling));
```


## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadinformation">GetThreadInformation</a>

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation">SetProcessInformation</a>
