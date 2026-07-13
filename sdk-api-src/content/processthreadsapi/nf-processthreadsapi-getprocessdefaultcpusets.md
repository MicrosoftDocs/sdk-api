---
UID: NF:processthreadsapi.GetProcessDefaultCpuSets
tech.root: processthreadsapi
title: GetProcessDefaultCpuSets
ms.date: 03/12/2021
ms.topic: language-reference
targetos: Windows
description: Retrieves the list of CPU Sets in the process default set that was set by SetProcessDefaultCpuSets.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll
req.header: processthreadsapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: kernel32.Lib
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
 - GetProcessDefaultCpuSets
f1_keywords:
 - GetProcessDefaultCpuSets
 - processthreadsapi/GetProcessDefaultCpuSets
dev_langs:
 - c++
---

## -description

Retrieves the list of CPU Sets in the process default set that was set by [**SetProcessDefaultCpuSets**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessdefaultcpusets). If no default CPU Sets are set for a given process, then the **RequiredIdCount** is set to 0 and the function succeeds.


## -parameters

### -param Process

Specifies a process handle for the process to query. This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right. The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) can also be specified here.


### -param CpuSetIds

Specifies an optional buffer to retrieve the list of CPU Set identifiers.

### -param CpuSetIdCount

Specifies the capacity of the buffer specified in **CpuSetIds**. If the buffer is NULL, this must be 0.

### -param RequiredIdCount

Specifies the required capacity of the buffer to hold the entire list of process default CPU Sets. On successful return, this specifies the number of IDs filled into the buffer.


## -returns

This API returns TRUE on success. If the buffer is not large enough the API returns FALSE, and the **GetLastError** value is ERROR\_INSUFFICIENT\_BUFFER. This API cannot fail when passed valid parameters and the return buffer is large enough.


## -remarks

## -see-also

