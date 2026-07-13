---
UID: NF:processthreadsapi.SetProcessDefaultCpuSetMasks
tech.root: processthreadsapi
title: SetProcessDefaultCpuSetMasks
ms.date: 08/05/2022
ms.topic: language-reference
targetos: Windows
description: The SetProcessDefaultCpuSetMasks function (processthreadsapi.h) sets the default CPU Sets assignment for threads in the specified process.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: kernel32.dll
req.header: processthreadsapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: kernel32.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11
req.target-min-winversvr: Windows Server 2022
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - kernel32.dll
 - api-ms-win-core-processthreads-l1-1-6
api_name:
 - SetProcessDefaultCpuSetMasks
f1_keywords:
 - SetProcessDefaultCpuSetMasks
 - processthreadsapi/SetProcessDefaultCpuSetMasks
helpviewer_keywords:
 - SetProcessDefaultCpuSetMasks
 - processthreadsapi/SetProcessDefaultCpuSetMasks
dev_langs:
 - c++
---

## -description

Sets the default CPU Sets assignment for threads in the specified process. 

## -parameters

### -param Process

Specifies the process for which to set the default CPU Sets. This handle must have the [PROCESS_SET_LIMITED_INFORMATION](/windows/win32/procthread/process-security-and-access-rights) access right. The value returned by [GetCurrentProcess](nf-processthreadsapi-getcurrentprocess.md) can also be specified here.

### -param CpuSetMasks

Specifies an optional buffer of [GROUP_AFFINITY](../winnt/ns-winnt-group_affinity.md) structures representing the CPU Sets to set as the process default CPU set. If this is NULL, the **SetProcessDefaultCpuSetMasks** function clears out any assignment.

### -param CpuSetMaskCount

Specifies the size of the *CpuSetMasks* array, in elements. If the buffer is NULL, this value must be zero. 

## -returns

This function cannot fail when passed valid parameters.

## -remarks

Threads belonging to this process which don’t have CPU Sets explicitly set using [SetThreadSelectedCpuSetMasks](nf-processthreadsapi-setthreadselectedcpusetmasks.md) or [SetThreadSelectedCpuSets](nf-processthreadsapi-setthreadselectedcpusets.md), will inherit the sets specified by **SetProcessDefaultCpuSetMasks** automatically.

This function is analogous to [SetProcessDefaultCpuSets](nf-processthreadsapi-setprocessdefaultcpusets.md), except that it uses group affinities as opposed to CPU Set IDs to represent a list of CPU sets. This means that the resulting process default CPU Set assignment is the set of all CPU sets with a home processor in the provided list of group affinities.

## -see-also

