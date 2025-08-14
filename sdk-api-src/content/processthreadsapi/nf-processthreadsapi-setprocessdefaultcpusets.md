---
UID: NF:processthreadsapi.SetProcessDefaultCpuSets
tech.root: processthreadsapi
title: SetProcessDefaultCpuSets
ms.date: 08/05/2022
ms.topic: language-reference
targetos: Windows
description: The SetProcessDefaultCpuSets function (processthreadsapi.h) sets the default CPU Sets assignment for threads in the specified process. 
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
 - SetProcessDefaultCpuSets
f1_keywords:
 - SetProcessDefaultCpuSets
 - processthreadsapi/SetProcessDefaultCpuSets
dev_langs:
 - c++
---

## -description

Sets the default CPU Sets assignment for threads in the specified process. Threads that are created, which don’t have CPU Sets explicitly set using [**SetThreadSelectedCpuSets**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadselectedcpusets), will inherit the sets specified by **SetProcessDefaultCpuSets** automatically.


## -parameters

### -param Process

Specifies the process for which to set the default CPU Sets. This handle must have the PROCESS\_SET\_LIMITED\_INFORMATION access right. The value returned by [**GetCurrentProcess**](nf-processthreadsapi-getcurrentprocess.md) can also be specified here.


### -param CpuSetIds

Specifies the list of CPU Set IDs to set as the process default CPU set. If this is NULL, the **SetProcessDefaultCpuSets** clears out any assignment.


### -param CpuSetIdCount

Specifies the number of IDs in the list passed in the **CpuSetIds** argument. If that value is NULL, this should be 0.


## -returns

This function cannot fail when passed valid parameters

## -remarks

## -see-also

