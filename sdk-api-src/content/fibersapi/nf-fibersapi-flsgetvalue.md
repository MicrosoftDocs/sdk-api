---
UID: NF:fibersapi.FlsGetValue
title: FlsGetValue function
description: Retrieves the value in the calling fiber's fiber local storage (FLS) slot for the specified FLS index. Each fiber has its own slot for each FLS index.
helpviewer_keywords: ["FlsGetValue","FlsGetValue function","_win32_flsgetvalue","base.flsgetvalue","fibersapi/FlsGetValue","winbase/FlsGetValue"]
old-location: base\flsgetvalue.htm
tech.root: backup
ms.assetid: 5d5a1fe6-10ed-42c5-87db-b24eef6f174c
ms.date: 12/05/2018
ms.keywords: FlsGetValue, FlsGetValue function, _win32_flsgetvalue, base.flsgetvalue, fibersapi/FlsGetValue, winbase/FlsGetValue
req.header: fibersapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - FlsGetValue
 - fibersapi/FlsGetValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-fibers-l1-1-2.dll
 - Kernel32.dll
 - API-MS-Win-Core-fibers-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-fibers-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - FlsGetValue
---

# FlsGetValue function


## -description

Retrieves the value in the calling fiber's fiber local storage (FLS) slot for the specified FLS index. Each fiber has its own slot for each FLS index.

## -parameters

### -param dwFlsIndex [in]

The FLS index that was allocated by the 
<a href="/windows/desktop/api/fibersapi/nf-fibersapi-flsalloc">FlsAlloc</a> function.

## -returns

If the function succeeds, the return value is the value stored in the calling fiber's FLS slot associated with the specified index.

If the function fails, the return value is NULL. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

FLS indexes are typically allocated by the 
<a href="/windows/desktop/api/fibersapi/nf-fibersapi-flsalloc">FlsAlloc</a> function during process or DLL initialization. After an FLS index is allocated, each fiber of the process can use it to access its own FLS slot for that index. A fiber specifies an FLS index in a call to 
<a href="/windows/desktop/api/fibersapi/nf-fibersapi-flssetvalue">FlsSetValue</a> to store a value in its slot. The thread specifies the same index in a subsequent call to 
<b>FlsSetValue</b> to retrieve the stored value.

## -see-also

<a href="/windows/desktop/ProcThread/fibers">Fibers</a>



<a href="/windows/desktop/api/fibersapi/nf-fibersapi-flsalloc">FlsAlloc</a>



<a href="/windows/desktop/api/fibersapi/nf-fibersapi-flssetvalue">FlsSetValue</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>