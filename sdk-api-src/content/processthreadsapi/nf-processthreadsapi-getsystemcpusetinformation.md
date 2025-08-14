---
UID: NF:processthreadsapi.GetSystemCpuSetInformation
tech.root: processthreadsapi
title: GetSystemCpuSetInformation
ms.date: 03/12/2021
ms.topic: language-reference
targetos: Windows
description: Allows an application to query the available CPU Sets on the system, and their current state.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: processthreadsapi.h
req.idl: Kernel32.dll
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: WIndows Server 2016
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
 - GetSystemCpuSetInformation
f1_keywords:
 - GetSystemCpuSetInformation
 - processthreadsapi/GetSystemCpuSetInformation
dev_langs:
 - c++
---

## -description

Allows an application to query the available CPU Sets on the system, and their current state.

## -parameters

### -param Information

A pointer to a [**SYSTEM\_CPU\_SET\_INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) structure that receives the CPU Set data. Pass NULL with a buffer length of 0 to determine the required buffer size.


### -param BufferLength

The length, in bytes, of the output buffer passed as the Information argument.

### -param ReturnedLength

The length, in bytes, of the valid data in the output buffer if the buffer is large enough, or the required size of the output buffer. If no CPU Sets exist, this value will be 0.

### -param Process

An optional handle to a process. This process is used to determine the value of the **AllocatedToTargetProcess** flag in the SYSTEM\_CPU\_SET\_INFORMATION structure. If a CPU Set is allocated to the specified process, the flag is set. Otherwise, it is clear. This handle must have the PROCESS\_QUERY\_LIMITED\_INFORMATION access right. The value returned by [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) may also be specified here.


### -param Flags

Reserved, must be 0.

## -returns

If the API succeeds it returns TRUE. If it fails, the error reason is available through **GetLastError**. If the Information buffer was NULL or not large enough, the error code ERROR\_INSUFFICIENT\_BUFFER is returned. This API cannot fail when passed valid parameters and a buffer that is large enough to hold all of the return data.


## -remarks

## -see-also

