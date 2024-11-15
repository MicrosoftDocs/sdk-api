---
UID: NF:processthreadsapi.TlsGetValue
title: TlsGetValue function (processthreadsapi.h)
description: Retrieves the value in the calling thread's thread local storage (TLS) slot for the specified TLS index. Each thread of a process has its own slot for each TLS index.
helpviewer_keywords: ["TlsGetValue","TlsGetValue function","_win32_tlsgetvalue","base.tlsgetvalue","processthreadsapi/TlsGetValue","winbase/TlsGetValue"]
old-location: base\tlsgetvalue.htm
tech.root: processthreadsapi
ms.assetid: 82bd5ff6-ff0b-42b7-9ece-e9e8531eb5fb
ms.date: 08/07/2024
ms.keywords: TlsGetValue, TlsGetValue function, _win32_tlsgetvalue, base.tlsgetvalue, processthreadsapi/TlsGetValue, winbase/TlsGetValue
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
 - TlsGetValue
 - processthreadsapi/TlsGetValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
 - TlsGetValue
---

# TlsGetValue function

## -description

Retrieves the value in the calling thread's thread local storage (TLS) slot for the specified TLS index. Each thread of a process has its own slot for each TLS index.

## -parameters

### -param dwTlsIndex [in]

The TLS index that was allocated by the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc">TlsAlloc</a> function.

## -returns

If the function succeeds, the return value is the value stored in the calling thread's TLS slot associated with the specified index. If <i>dwTlsIndex</i> is a valid index allocated by a successful call to <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc">TlsAlloc</a>, this function always succeeds.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The data stored in a TLS slot can have a value of 0 because it still has its initial value or because the thread called the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlssetvalue">TlsSetValue</a> function with 0. Therefore, if the return value is 0, you must check whether <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_SUCCESS</b> before determining that the function has failed. If <b>GetLastError</b> returns <b>ERROR_SUCCESS</b>, then the function has succeeded and the data stored in the TLS slot is 0. Otherwise, the function has failed.

Functions that return indications of failure call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror">SetLastError</a> when they fail. They generally do not call <b>SetLastError</b> when they succeed. The <b>TlsGetValue</b> function is an exception to this general rule. The <b>TlsGetValue</b> function calls <b>SetLastError</b> to clear a thread's last error when it succeeds. That allows checking for the error-free retrieval of zero values.

## -remarks

<b>Windows 8.1</b>, <b>Windows Server 2012 R2</b>, and <b>Windows 10, version 1507</b>: This function is supported for Windows Store apps on Windows 8.1, Windows Server 2012 R2, and Windows 10, version 1507. When a Windows Store app calls this function, it is replaced with an inline call to <b>FlsGetValue</b>. Refer to <a href="/windows/desktop/api/fibersapi/nf-fibersapi-flsgetvalue">FlsGetValue</a> for function documentation.

<b>Windows 10, version 1511</b> and <b>Windows 10, version 1607</b>: This function is fully supported for Universal Windows Platform (UWP) apps, and is no longer replaced with an inline call to <b>FlsGetValue</b>.

TLS indexes are typically allocated by the [TlsAlloc](nf-processthreadsapi-tlsalloc.md) function during process or DLL initialization. After a TLS index is allocated, each thread of the process can use it to access its own TLS slot for that index. A thread specifies a TLS index in a call to [TlsSetValue](nf-processthreadsapi-tlssetvalue.md) to store a value in its slot. The thread specifies the same index in a subsequent call to <b>TlsGetValue</b> to retrieve the stored value.

<b>TlsGetValue</b> was implemented with speed as the primary goal. The function performs minimal parameter validation and error checking. In particular, it succeeds if <i>dwTlsIndex</i> is in the range 0 through (<b>TLS_MINIMUM_AVAILABLE</b>– 1). It is up to the programmer to ensure that the index is valid and that the thread calls [TlsSetValue](nf-processthreadsapi-tlssetvalue.md) before calling <b>TlsGetValue</b>.

<b>TlsGetValue</b> always sets a thread's last error. In some cases, an application (such as those with custom heaps that support malloc) may need to call <b>GetLastError</b> before calling <b>TlsGetValue</b> to save the thread's last error (followed by <b>SetLastError</b> to restore the saved error). Unfortunately, this can incur a non-trivial performance cost on certain CPUs. 

**Windows 11 24H2 and later:** Use the [**TlsGetValue2**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue2) function, which is identical to <b>TlsGetValue</b> except that it doesn't set the thread's last error. Applications calling <b>TlsGetValue2</b> should avoid using 0 as a valid value because <b>GetLastError</b> cannot be called to check if <b>TlsGetValue2</b> failed.

#### Examples

For an example, see <a href="/windows/desktop/ProcThread/using-thread-local-storage">Using Thread Local Storage</a> or <a href="/windows/desktop/Dlls/using-thread-local-storage-in-a-dynamic-link-library">Using Thread Local Storage in a Dynamic-Link Library</a>.

## -see-also

[**TlsGetValue2**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-tlsgetvalue2)

[Process and Thread Functions](/windows/win32/ProcThread/process-and-thread-functions)

[Thread Local Storage](/windows/win32/ProcThread/thread-local-storage)

[TlsAlloc](nf-processthreadsapi-tlsalloc.md)

[TlsFree](nf-processthreadsapi-tlsfree.md)

[TlsSetValue](nf-processthreadsapi-tlssetvalue.md)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
