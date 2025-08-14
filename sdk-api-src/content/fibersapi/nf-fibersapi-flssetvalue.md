---
UID: NF:fibersapi.FlsSetValue
title: FlsSetValue function
description: Stores a value in the calling fiber's fiber local storage (FLS) slot for the specified FLS index. Each fiber has its own slot for each FLS index.
helpviewer_keywords: ["FlsSetValue","FlsSetValue function","_win32_flssetvalue","base.flssetvalue","fibersapi/FlsSetValue","winbase/FlsSetValue"]
old-location: base\flssetvalue.htm
tech.root: backup
ms.assetid: f2abea00-8c1b-47e8-a4e9-9e3e7242d0ad
ms.date: 12/05/2018
ms.keywords: FlsSetValue, FlsSetValue function, _win32_flssetvalue, base.flssetvalue, fibersapi/FlsSetValue, winbase/FlsSetValue
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
 - FlsSetValue
 - fibersapi/FlsSetValue
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
 - FlsSetValue
---

# FlsSetValue function


## -description

Stores a value in the calling fiber's fiber local storage (FLS) slot for the specified FLS index. Each fiber has its own slot for each FLS index.

## -parameters

### -param dwFlsIndex [in]

The FLS index that was allocated by the 
<a href="/windows/desktop/api/fibersapi/nf-fibersapi-flsalloc">FlsAlloc</a> function.

### -param lpFlsData [in, optional]

The value to be stored in the FLS slot for the calling fiber.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following errors can be returned.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The index is not in range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The FLS array has not been allocated.

</td>
</tr>
</table>

## -remarks

FLS indexes are typically allocated by the 
<a href="/windows/desktop/api/fibersapi/nf-fibersapi-flsalloc">FlsAlloc</a> function during process or DLL initialization. After an FLS index is allocated, each fiber of the process can use it to access its own FLS slot for that index. A thread specifies an FLS index in a call to 
<b>FlsSetValue</b> to store a value in its slot. The thread specifies the same index in a subsequent call to 
<a href="/windows/desktop/api/fibersapi/nf-fibersapi-flsgetvalue">FlsGetValue</a> to retrieve the stored value.

## -see-also

<a href="/windows/desktop/ProcThread/fibers">Fibers</a>



<a href="/windows/desktop/api/fibersapi/nf-fibersapi-flsalloc">FlsAlloc</a>



<a href="/windows/desktop/api/fibersapi/nf-fibersapi-flsgetvalue">FlsGetValue</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>