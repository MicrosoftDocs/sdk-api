---
UID: NF:processthreadsapi.TlsGetValue2
tech.root: processthreadsapi
title: TlsGetValue2 function (processthreadsapi.h)
ms.date: 08/07/2024
ms.keywords: TlsGetValue2, TlsGetValue2 function, _win32_tlsgetvalue2, base.tlsgetvalue2, processthreadsapi/TlsGetValue2, winbase/TlsGetValue2
targetos: Windows
description: Retrieves the value in the calling thread's thread local storage (TLS) slot for the specified TLS index. Each thread of a process has its own slot for each TLS index.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.header: processthreadsapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11, version 24H2
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - processthreadsapi.h
api_name:
 - TlsGetValue2
f1_keywords:
 - TlsGetValue2
 - processthreadsapi/TlsGetValue2
dev_langs:
 - c++
helpviewer_keywords:
 - TlsGetValue2
---

## -description

Retrieves the value in the calling thread's thread local storage (TLS) slot for the specified TLS index. Each thread of a process has its own slot for each TLS index.

## -parameters

### -param dwTlsIndex [in]

The TLS index that was allocated by the [TlsAlloc function](nf-processthreadsapi-tlsalloc.md).

## -returns

If the function succeeds, the return value is the value stored in the calling thread's TLS slot associated with the specified index. If *dwTlsIndex* is a valid index allocated by a successful call to [TlsAlloc](nf-processthreadsapi-tlsalloc.md), this function always succeeds.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

The data stored in a TLS slot can have a value of 0 because it still has its initial value or because the thread called the [TlsSetValue function](nf-processthreadsapi-tlssetvalue.md) with 0. Therefore, if the return value is 0, you must check whether [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md) returns **ERROR_SUCCESS** before determining that the function has failed. If **GetLastError** returns **ERROR_SUCCESS**, then the function has succeeded and the data stored in the TLS slot is 0. Otherwise, the function has failed.

Functions that return indications of failure call [SetLastError](../errhandlingapi/nf-errhandlingapi-setlasterror.md) when they fail. They generally do not call **SetLastError** when they succeed. The **TlsGetValue** function is an exception to this general rule. The **TlsGetValue** function calls **SetLastError** to clear a thread's last error when it succeeds. That allows checking for the error-free retrieval of zero values.

## -remarks

TLS indexes are typically allocated by the [TlsAlloc](nf-processthreadsapi-tlsalloc.md) function during process or DLL initialization. After a TLS index is allocated, each thread of the process can use it to access its own TLS slot for that index. A thread specifies a TLS index in a call to [TlsSetValue](nf-processthreadsapi-tlssetvalue.md) to store a value in its slot. The thread specifies the same index in a subsequent call to **TlsGetValue** to retrieve the stored value.

**TlsGetValue** was implemented with speed as the primary goal. The function performs minimal parameter validation and error checking. In particular, it succeeds if *dwTlsIndex* is in the range 0 through (**TLS_MINIMUM_AVAILABLE**– 1). It is up to the programmer to ensure that the index is valid and that the thread calls [TlsSetValue](nf-processthreadsapi-tlssetvalue.md) before calling **TlsGetValue**.

This function is identical to [**TlsGetValue**](nf-processthreadsapi-tlsgetvalue.md) except that it doesn't set the thread's last error. Applications calling this function should avoid using 0 as a valid value, because **GetLastError** cannot be called to check if the function failed.

### Examples

See [Using Thread Local Storage](/windows/desktop/ProcThread/using-thread-local-storage) or [Using Thread Local Storage in a Dynamic-Link Library](/windows/desktop/Dlls/using-thread-local-storage-in-a-dynamic-link-library).

## -see-also

[Process and Thread Functions](/windows/win32/ProcThread/process-and-thread-functions)

[Thread Local Storage](/windows/win32/ProcThread/thread-local-storage)

[TlsAlloc](nf-processthreadsapi-tlsalloc.md)

[TlsFree](nf-processthreadsapi-tlsfree.md)

[TlsSetValue](nf-processthreadsapi-tlssetvalue.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
