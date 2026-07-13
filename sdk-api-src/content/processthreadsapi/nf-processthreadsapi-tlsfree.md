---
UID: NF:processthreadsapi.TlsFree
title: TlsFree function (processthreadsapi.h)
description: Releases a thread local storage (TLS) index, making it available for reuse.
helpviewer_keywords: ["TlsFree","TlsFree function","_win32_tlsfree","base.tlsfree","processthreadsapi/TlsFree","winbase/TlsFree"]
old-location: base\tlsfree.htm
tech.root: processthreadsapi
ms.assetid: f5b1e8fc-02eb-4a06-b606-2b647944029b
ms.date: 02/02/2024
ms.keywords: TlsFree, TlsFree function, _win32_tlsfree, base.tlsfree, processthreadsapi/TlsFree, winbase/TlsFree
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
 - TlsFree
 - processthreadsapi/TlsFree
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
 - TlsFree
---

# TlsFree function

## -description

Releases a thread local storage (TLS) index, making it available for reuse.

## -parameters

### -param dwTlsIndex [in]

The TLS index that was allocated by the <a href="/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsalloc">TlsAlloc</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>Windows Phone 8.1:</b> This function is supported for Windows Phone Store apps on Windows Phone 8.1 and later. When a Windows Phone Store app calls this function, it is replaced with an inline call to <b>FlsFree</b>. Refer to <a href="/windows/win32/api/fibersapi/nf-fibersapi-flsfree">FlsFree</a> for function documentation.

<b>Windows 8.1</b>, <b>Windows Server 2012 R2</b>, and <b>Windows 10, version 1507</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and Windows 10, version 1507. When a Windows Store app calls this function, it is replaced with an inline call to <b>FlsFree</b>. Refer to <a href="/windows/win32/api/fibersapi/nf-fibersapi-flsfree">FlsFree</a> for function documentation.

<b>Windows 10, version 1511</b> and <b>Windows 10, version 1607</b>: This function is fully supported for Universal Windows Platform (UWP) apps, and is no longer replaced with an inline call to <b>FlsFree</b>.

If the threads of the process have allocated memory and stored a pointer to the memory in a TLS slot, they should free the memory before calling 
<b>TlsFree</b>. The <b>TlsFree</b> function does not free memory blocks whose addresses have been stored in the TLS slots associated with the TLS index. It is expected that DLLs call this function (if at all) only during <b>DLL_PROCESS_DETACH</b>.

For more information, see [Thread Local Storage](/windows/win32/ProcThread/thread-local-storage).

#### Examples

For an example, see <a href="/windows/win32/ProcThread/using-thread-local-storage">Using Thread Local Storage</a> or <a href="/windows/win32/Dlls/using-thread-local-storage-in-a-dynamic-link-library">Using Thread Local Storage in a Dynamic-Link Library</a>.

## -see-also

[Processes and Threads Overview](/windows/win32/ProcThread/processes-and-threads)

[Thread Local Storage](/windows/win32/ProcThread/thread-local-storage)

[TlsAlloc](nf-processthreadsapi-tlsalloc.md)

[TlsGetValue](nf-processthreadsapi-tlsgetvalue.md)

[TlsSetValue](nf-processthreadsapi-tlssetvalue.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
