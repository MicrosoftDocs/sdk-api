---
UID: NF:processthreadsapi.TlsSetValue
title: TlsSetValue function (processthreadsapi.h)
description: Stores a value in the calling thread's thread local storage (TLS) slot for the specified TLS index. Each thread of a process has its own slot for each TLS index.
helpviewer_keywords: ["TlsSetValue","TlsSetValue function","_win32_tlssetvalue","base.tlssetvalue","processthreadsapi/TlsSetValue","winbase/TlsSetValue"]
old-location: base\tlssetvalue.htm
tech.root: processthreadsapi
ms.assetid: 531b4a4a-a251-4ab4-b00a-754783a51283
ms.date: 02/02/2024
ms.keywords: TlsSetValue, TlsSetValue function, _win32_tlssetvalue, base.tlssetvalue, processthreadsapi/TlsSetValue, winbase/TlsSetValue
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
 - TlsSetValue
 - processthreadsapi/TlsSetValue
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
 - TlsSetValue
---

# TlsSetValue function

## -description

Stores a value in the calling thread's thread local storage (TLS) slot for the specified TLS index. Each thread of a process has its own slot for each TLS index.

## -parameters

### -param dwTlsIndex [in]

The TLS index that was allocated by the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc">TlsAlloc</a> function.

### -param lpTlsValue [in, optional]

The value to be stored in the calling thread's TLS slot for the index.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later. When a Windows Phone Store app calls this function, it is replaced with an inline call to <b>FlsSetValue</b>. Refer to <a href="/windows/desktop/api/fibersapi/nf-fibersapi-flssetvalue">FlsSetValue</a> for function documentation.

<b>Windows 8.1</b>, <b>Windows Server 2012 R2</b>, and <b>Windows 10, version 1507</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and Windows 10, version 1507. When a Windows Store app calls this function, it is replaced with an inline call to <b>FlsSetValue</b>. Refer to <a href="/windows/desktop/api/fibersapi/nf-fibersapi-flssetvalue">FlsSetValue</a> for function documentation.

<b>Windows 10, version 1511</b> and <b>Windows 10, version 1607</b>: This function is fully supported for Universal Windows Platform (UWP) apps, and is no longer replaced with an inline call to <b>FlsSetValue</b>.

TLS indexes are typically allocated by the [TlsAlloc](nf-processthreadsapi-tlsalloc.md) function during process or DLL initialization. When a TLS index is allocated, its storage slots are initialized to NULL. After a TLS index is allocated, each thread of the process can use it to access its own TLS slot for that index. A thread specifies a TLS index in a call to <b>TlsSetValue</b>, to store a value in its slot. The thread specifies the same index in a subsequent call to [TlsGetValue](nf-processthreadsapi-tlsgetvalue.md), to retrieve the stored value.

<b>TlsSetValue</b> was implemented with speed as the primary goal. The function performs minimal parameter validation and error checking. In particular, it succeeds if <i>dwTlsIndex</i> is in the range 0 through (<b>TLS_MINIMUM_AVAILABLE </b>– 1). It is up to the programmer to ensure that the index is valid before calling [TlsGetValue](nf-processthreadsapi-tlsgetvalue.md).

#### Examples

For an example, see <a href="/windows/win32/ProcThread/using-thread-local-storage">Using Thread Local Storage</a> or <a href="/windows/win32/Dlls/using-thread-local-storage-in-a-dynamic-link-library">Using Thread Local Storage in a Dynamic-Link Library</a>.

## -see-also

[Process and Thread Functions](/windows/win32/ProcThread/process-and-thread-functions)

[Thread Local Storage](/windows/win32/ProcThread/thread-local-storage)

[TlsAlloc](nf-processthreadsapi-tlsalloc.md)

[TlsFree](nf-processthreadsapi-tlsfree.md)

[TlsGetValue](nf-processthreadsapi-tlsgetvalue.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
