---
UID: NF:processthreadsapi.GetCurrentThread
title: GetCurrentThread function (processthreadsapi.h)
description: Retrieves a pseudo handle for the calling thread.
helpviewer_keywords: ["GetCurrentThread","GetCurrentThread function","_win32_getcurrentthread","base.getcurrentthread","processthreadsapi/GetCurrentThread","winbase/GetCurrentThread"]
old-location: base\getcurrentthread.htm
tech.root: processthreadsapi
ms.assetid: 91a11552-66c1-42bd-b837-8a7685977bc9
ms.date: 02/02/2024
ms.keywords: GetCurrentThread, GetCurrentThread function, _win32_getcurrentthread, base.getcurrentthread, processthreadsapi/GetCurrentThread, winbase/GetCurrentThread
req.header: processthreadsapi.h
req.include-header: Windows.h on Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetCurrentThread
 - processthreadsapi/GetCurrentThread
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
 - Kernel32.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-1.dll
 - API-MS-Win-Core-ProcessThreads-l1-1-2.dll
 - api-ms-win-downlevel-kernel32-l1-1-0.dll
 - API-MS-Win-Core-ProcessThreads-L1-1-3.dll
 - Vertdll.dll
api_name:
 - GetCurrentThread
---

# GetCurrentThread function

## -description

Retrieves a pseudo handle for the calling thread.

## -returns

The return value is a pseudo handle for the current thread.

## -remarks

A pseudo handle is a special constant that is interpreted as the current thread handle. The calling thread can use this handle to specify itself whenever a thread handle is required. Pseudo handles are not inherited by child processes.

This handle has the <b>THREAD_ALL_ACCESS</b> access right to the thread object. For more information, see 
<a href="/windows/win32/ProcThread/thread-security-and-access-rights">Thread Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>This handle has the maximum access allowed by the security descriptor of the thread to the primary token of the process.

The function cannot be used by one thread to create a handle that can be used by other threads to refer to the first thread. The handle is always interpreted as referring to the thread that is using it. A thread can create a "real" handle to itself that can be used by other threads, or inherited by other processes, by specifying the pseudo handle as the source handle in a call to the <a href="/windows/win32/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a> function.

The pseudo handle need not be closed when it is no longer needed. Calling the 
<a href="/windows/win32/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function with this handle has no effect. If the pseudo handle is duplicated by 
<a href="/windows/win32/api/handleapi/nf-handleapi-duplicatehandle">DuplicateHandle</a>, the duplicate handle must be closed.

Do not create a thread while impersonating a security context. The call will succeed, however the newly created thread will have reduced access rights to itself when calling <b>GetCurrentThread</b>. The access rights granted this thread will  be derived from the access rights the impersonated user has to the process. Some access rights including <b>THREAD_SET_THREAD_TOKEN</b> and <b>THREAD_GET_CONTEXT</b> may not be present, leading to unexpected failures.

#### Examples

For an example, see <a href="/windows/win32/SecAuthZ/verifying-client-access-with-acls-in-c--">Checking Client Access</a>.

## -see-also

[CloseHandle](../handleapi/nf-handleapi-closehandle.md)

[DuplicateHandle](../handleapi/nf-handleapi-duplicatehandle.md)

[GetCurrentProcess](nf-processthreadsapi-getcurrentprocess.md)

[GetCurrentThreadId](nf-processthreadsapi-getcurrentthreadid.md)

[OpenThread](nf-processthreadsapi-openthread.md)

[Process and Thread Functions](/windows/win32/ProcThread/process-and-thread-functions)

[Threads](/windows/win32/ProcThread/multiple-threads)

[Vertdll APIs available in VBS enclaves](/windows/win32/trusted-execution/enclaves-available-in-vertdll)
