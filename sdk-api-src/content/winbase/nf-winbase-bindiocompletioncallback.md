---
UID: NF:winbase.BindIoCompletionCallback
title: BindIoCompletionCallback function (winbase.h)
description: Associates the I/O completion port owned by the thread pool with the specified file handle. On completion of an I/O request involving this file, a non-I/O worker thread will execute the specified callback function.
helpviewer_keywords: ["BindIoCompletionCallback","BindIoCompletionCallback function","_win32_bindiocompletioncallback","base.bindiocompletioncallback","winbase/BindIoCompletionCallback"]
old-location: base\bindiocompletioncallback.htm
tech.root: backup
ms.assetid: 2eb18e84-6d6b-4b11-8e8f-6110fa44b7f9
ms.date: 12/05/2018
ms.keywords: BindIoCompletionCallback, BindIoCompletionCallback function, _win32_bindiocompletioncallback, base.bindiocompletioncallback, winbase/BindIoCompletionCallback
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - BindIoCompletionCallback
 - winbase/BindIoCompletionCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - BindIoCompletionCallback
---

# BindIoCompletionCallback function


## -description

Associates the I/O completion port owned by the <a href="/windows/desktop/ProcThread/thread-pooling">thread pool</a> with the specified file handle. On completion of an I/O request involving this file, a non-I/O worker thread will execute the specified callback function.

## -parameters

### -param FileHandle [in]

A handle to the file opened for overlapped I/O completion. This handle is returned by the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function, with the <b>FILE_FLAG_OVERLAPPED</b> flag.

### -param Function [in]

A pointer to the callback function to be executed in a non-I/O worker thread when the I/O operation is complete. This callback function must not call the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread">TerminateThread</a> function.

For more information about the completion routine, see 
<a href="/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine">FileIOCompletionRoutine</a>.

### -param Flags [in]

This parameter must be zero.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

The callback function might not be executed if the process issues an asynchronous request on the file specified by the <i>FileHandle</i> parameter but the request returns immediately with an error code other than ERROR_IO_PENDING.

Be sure that the thread that initiates the asynchronous I/O request does not terminate before the request is completed. Also, if a function in a DLL is queued to a worker thread, be sure that the function in the DLL has completed execution before the DLL is unloaded.

The thread pool maintains an I/O completion port. When you call <b>BindIoCompletionCallback</b>, it associates the specified file with the thread pool's I/O completion port. Asynchronous requests on that file object will complete by posting to the completion port, where they will be picked up by thread pool worker threads. For callbacks that must issue an I/O request that completes as an asynchronous procedure call, the thread pool provides an I/O worker pool. The I/O worker threads do not wait on the completion port; they sleep in an alertable wait state so that I/O request packets that complete can wake them up. Both types of worker threads check whether there is I/O pending on them and if there is, they do not exit. For more information, see <a href="/windows/desktop/Sync/asynchronous-procedure-calls">Asynchronous Procedure Calls</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/minwinbase/nc-minwinbase-lpoverlapped_completion_routine">FileIOCompletionRoutine</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/ProcThread/thread-pooling">Thread Pooling</a>
