---
UID: NF:processthreadsapi.SetThreadSelectedCpuSetMasks
tech.root: processthreadsapi
title: SetThreadSelectedCpuSetMasks
ms.date: 03/12/2021
ms.topic: language-reference
targetos: Windows
description: Sets the selected CPU Sets assignment for the specified thread. This assignment overrides the process default assignment, if one is set. (SetThreadSelectedCpuSetMasks)
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: kernel32.dll
req.header: processthreadsapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
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
 - SetThreadSelectedCpuSetMasks
f1_keywords:
 - SetThreadSelectedCpuSetMasks
 - processthreadsapi/SetThreadSelectedCpuSetMasks
offlinehelp_keywords:
 - SetThreadSelectedCpuSetMasks
 - processthreadsapi/SetThreadSelectedCpuSetMasks
dev_langs:
 - c++
---

## -description

Sets the selected CPU Sets assignment for the specified thread. This assignment overrides the process default assignment, if one is set.

## -parameters

### -param Thread

Specifies the thread on which to set the CPU Set assignment. [PROCESS_SET_LIMITED_INFORMATION](/windows/win32/procthread/process-security-and-access-rights) access right. The value returned by [GetCurrentProcess](nf-processthreadsapi-getcurrentprocess.md) can also be specified here.

### -param CpuSetMasks

Specifies an optional buffer of [GROUP_AFFINITY](../winnt/ns-winnt-group_affinity.md) structures representing the CPU Sets to set as the thread selected CPU set. If this is NULL, the **SetThreadSelectedCpuSetMasks** function clears out any assignment, reverting to process default assignment if one is set.

### -param CpuSetMaskCount

Specifies the number of **GROUP_AFFINITY** structures in the list passed in the GroupCpuSets argument. If the buffer is NULL, this value must be zero. 

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero and extended error information can be retrieved by calling [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md). 


## -remarks

This function is analogous to [SetThreadSelectedCpuSets](nf-processthreadsapi-setthreadselectedcpusets.md), except that it uses group affinities as opposed to CPU Set IDs to represent a list of CPU sets. This means that the resulting thread selected CPU Set assignment is the set of all CPU sets with a home processor in the provided list of group affinities.

## -see-also

