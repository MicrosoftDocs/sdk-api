---
UID: NF:processthreadsapi.TlsAlloc
title: TlsAlloc function (processthreadsapi.h)
description: Allocates a thread local storage (TLS) index. Any thread of the process can subsequently use this index to store and retrieve values that are local to the thread, because each thread receives its own slot for the index.
helpviewer_keywords: ["TlsAlloc","TlsAlloc function","_win32_tlsalloc","base.tlsalloc","processthreadsapi/TlsAlloc","winbase/TlsAlloc"]
old-location: base\tlsalloc.htm
tech.root: processthreadsapi
ms.assetid: cbb3d832-cd92-4875-8366-6b69be7a536f
ms.date: 12/05/2024
ms.keywords: TlsAlloc, TlsAlloc function, _win32_tlsalloc, base.tlsalloc, processthreadsapi/TlsAlloc, winbase/TlsAlloc
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
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
req.lib: Kernel32.lib; WindowsPhoneCore.lib on Windows Phone 8.1
req.dll: KernelBase.dll on Windows Phone 8.1; Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TlsAlloc
 - processthreadsapi/TlsAlloc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-processthreads-l1-1-8.dll
 - api-ms-win-core-processthreads-l1-1-7.dll
 - api-ms-win-core-processthreads-l1-1-6.dll
 - api-ms-win-core-processthreads-l1-1-5.dll
 - api-ms-win-core-processthreads-l1-1-4.dll
 - KernelBase.dll
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
 - vertdll.dll
api_name:
 - TlsAlloc
---

# TlsAlloc function

## -description

Allocates a thread local storage (TLS) index. Any thread of the process can subsequently use this index to store and retrieve values that are local to the thread, because each thread receives its own slot for the index.

## -returns

If the function succeeds, the return value is a TLS index. The slots for the index are initialized to zero.

If the function fails, the return value is <b>TLS_OUT_OF_INDEXES</b>. To get extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later. When a Windows Phone Store app calls this function, it is replaced with an inline call to <b>FlsAlloc</b>. Refer to <a href="/windows/win32/api/fibersapi/nf-fibersapi-flsalloc">FlsAlloc</a> for function documentation.

<b>Windows 8.1</b>,  <b>Windows Server 2012 R2</b>, and <b>Windows 10, version 1507</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and Windows 10, version 1507. When a Windows Store app calls this function, it is replaced with an inline call to <b>FlsAlloc</b>. Refer to <a href="/windows/win32/api/fibersapi/nf-fibersapi-flsalloc">FlsAlloc</a> for function documentation.

<b>Windows 10, version 1511</b> and <b>Windows 10, version 1607</b>: This function is fully supported for Universal Windows Platform (UWP) apps, and is no longer replaced with an inline call to <b>FlsAlloc</b>.

The threads of the process can use the TLS index in subsequent calls to the <a href="/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsfree">TlsFree</a>, <a href="/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlssetvalue">TlsSetValue</a>, or <a href="/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue">TlsGetValue</a> functions. The value of the TLS index should be treated as an opaque value; do not assume that it is an index into a zero-based array.

TLS indexes are typically allocated during process or dynamic-link library (DLL) initialization. When a TLS index is allocated, its storage slots are initialized to <b>NULL</b>. After a TLS index has been allocated, each thread of the process can use it to access its own TLS storage slot. To store a value in its TLS slot, a thread specifies the index in a call to [TlsSetValue](nf-processthreadsapi-tlssetvalue.md). The thread specifies the same index in a subsequent call to [TlsGetValue](nf-processthreadsapi-tlsgetvalue.md), to retrieve the stored value.

TLS indexes are not valid across process boundaries. A DLL cannot assume that an index assigned in one process is valid in another process.

#### Examples

For an example, see <a href="/windows/win32/ProcThread/using-thread-local-storage">Using Thread Local Storage</a> or <a href="/windows/win32/Dlls/using-thread-local-storage-in-a-dynamic-link-library">Using Thread Local Storage in a Dynamic-Link Library</a>.

## -see-also

[Process and Thread Functions](/windows/win32/ProcThread/process-and-thread-functions)

[Thread Local Storage](/windows/win32/ProcThread/thread-local-storage)

[TlsFree](nf-processthreadsapi-tlsfree.md)

[TlsGetValue](nf-processthreadsapi-tlsgetvalue.md)

[TlsSetValue](nf-processthreadsapi-tlssetvalue.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
