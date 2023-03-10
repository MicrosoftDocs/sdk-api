---
UID: NF:processthreadsapi.GetThreadSelectedCpuSetMasks
tech.root: ProcThread
title: GetThreadSelectedCpuSetMasks
ms.date: 03/12/2021
ms.topic: language-reference
targetos: Windows
description: Returns the explicit CPU Set assignment of the specified thread, if any assignment was set using SetThreadSelectedCpuSetMasks or SetThreadSelectedCpuSets.
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
 - kernel32.dll
 - api-ms-win-core-processthreads-l1-1-6
api_name:
 - GetThreadSelectedCpuSetMasks
f1_keywords:
 - GetThreadSelectedCpuSetMasks
 - processthreadsapi/GetThreadSelectedCpuSetMasks
helpviewer_keywords:
 - GetThreadSelectedCpuSetMasks
 - processthreadsapi/GetThreadSelectedCpuSetMasks
dev_langs:
 - c++
---

## -description

Returns the explicit CPU Set assignment of the specified thread, if any assignment was set using [SetThreadSelectedCpuSetMasks](nf-processthreadsapi-setthreadselectedcpusetmasks.md) or [SetThreadSelectedCpuSets](nf-processthreadsapi-setthreadselectedcpusets.md). 

## -parameters

### -param Thread

Specifies the thread for which to query the selected CPU Sets. This handle must have the [PROCESS_QUERY_LIMITED_INFORMATION](/windows/win32/procthread/process-security-and-access-rights) access right. The value returned by [GetCurrentProcess](nf-processthreadsapi-getcurrentprocess.md) can also be specified here.

### -param CpuSetMasks

Specifies an optional buffer to retrieve a list of [GROUP_AFFINITY](../winnt/ns-winnt-group_affinity.md) structures representing the thread selected CPU Sets.

### -param CpuSetMaskCount

Specifies the size of the *CpuSetMasks* array, in elements.

### -param RequiredMaskCount

On successful return, specifies the number of affinity structures written to the array.
If the array is too small, the function fails with **ERROR_INSUFFICIENT_BUFFER** and sets the *RequiredMaskCount* parameter to the number of elements required.
The number of required elements is always less than or equal to the maximum group count returned by [GetMaximumProcessorGroupCount](../winbase/nf-winbase-getmaximumprocessorgroupcount.md).



## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero and extended error information can be retrieved by calling [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md). 

If the array supplied is too small, the error value is **ERROR_INSUFFICIENT_BUFFER** and the RequiredMaskCount is set to the number of elements required.




## -remarks

If no explicit assignment is set, *RequiredMaskCount* is set to 0 and the function succeeds.

This function is analogous to [GetThreadSelectedCpuSets](nf-processthreadsapi-getthreadselectedcpusets.md), except that it uses group affinities as opposed to CPU Set IDs to represent a list of CPU sets. This means that the thread selected CPU Sets are mapped to their home processors, and those processors are retrieved in the resulting list of group affinities.

## -see-also

