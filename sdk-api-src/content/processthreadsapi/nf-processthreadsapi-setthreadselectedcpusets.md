---
UID: NF:processthreadsapi.SetThreadSelectedCpuSets
tech.root: processthreadsapi
title: SetThreadSelectedCpuSets
ms.date: 03/12/2021
ms.topic: language-reference
targetos: Windows
description: Sets the selected CPU Sets assignment for the specified thread. This assignment overrides the process default assignment, if one is set. (SetThreadSelectedCpuSets)
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
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - api-ms-win-core-processthreads-l1-1-3.dll
 - kernel32.dll
 - api-ms-win-core-processthreads-l1-1-6
api_name:
 - SetThreadSelectedCpuSets
f1_keywords:
 - SetThreadSelectedCpuSets
 - processthreadsapi/SetThreadSelectedCpuSets
dev_langs:
 - c++
---

## -description

Sets the selected CPU Sets assignment for the specified thread. This assignment overrides the process default assignment, if one is set.


## -parameters

### -param Thread

Specifies the thread on which to set the CPU Set assignment. This handle must have the THREAD\_SET\_LIMITED\_INFORMATION access right. The value returned by [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) can also be used.


### -param CpuSetIds

Specifies the list of CPU Set IDs to set as the thread selected CPU set. If this is NULL, the API clears out any assignment, reverting to process default assignment if one is set.


### -param CpuSetIdCount

Specifies the number of IDs in the list passed in the **CpuSetIds** argument. If that value is NULL, this should be 0.


## -returns

If the function succeeds, the return value is nonzero.

This function cannot fail when passed valid parameters.

## -remarks

## -see-also

