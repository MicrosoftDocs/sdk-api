---
UID: NF:processthreadsapi.GetThreadSelectedCpuSets
tech.root: processthreadsapi
title: GetThreadSelectedCpuSets
ms.date: 03/15/2021
ms.topic: language-reference
targetos: Windows
description: Returns the explicit CPU Set assignment of the specified thread, if any assignment was set using the SetThreadSelectedCpuSets API. 
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
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
- DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
 - KernelBase.dll
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
api_name:
 - GetThreadSelectedCpuSets
f1_keywords:
 - GetThreadSelectedCpuSets
 - processthreadsapi/GetThreadSelectedCpuSets
dev_langs:
 - c++
---

## -description

Returns the explicit CPU Set assignment of the specified thread, if any assignment was set using the [**SetThreadSelectedCpuSets**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadselectedcpusets) API. If no explicit assignment is set, **RequiredIdCount** is set to 0 and the function returns TRUE.


## -parameters

### -param Thread

Specifies the thread for which to query the selected CPU Sets. This handle must have the THREAD\_QUERY\_LIMITED\_INFORMATION access right. The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be specified here.


### -param CpuSetIds

Specifies an optional buffer to retrieve the list of CPU Set identifiers.

### -param CpuSetIdCount

Specifies the capacity of the buffer specified in **CpuSetIds**. If the buffer is NULL, this must be 0.

### -param RequiredIdCount

Specifies the required capacity of the buffer to hold the entire list of thread selected CPU Sets. On successful return, this specifies the number of IDs filled into the buffer.


## -returns

This API returns TRUE on success. If the buffer is not large enough, the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER. This API cannot fail when passed valid parameters and the return buffer is large enough.


## -remarks

## -see-also

