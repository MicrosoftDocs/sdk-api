---
UID: NC:minwinbase.LPOVERLAPPED_COMPLETION_ROUTINE
title: LPOVERLAPPED_COMPLETION_ROUTINE (minwinbase.h)
description: An application-defined callback function used with the ReadFileEx and WriteFileEx functions. It is called when the asynchronous input and output (I/O) operation is completed or canceled and the calling thread is in an alertable state.
helpviewer_keywords: ["FileIOCompletionRoutine","FileIOCompletionRoutine callback","FileIOCompletionRoutine callback function [Files]","LPOVERLAPPED_COMPLETION_ROUTINE","LPOVERLAPPED_COMPLETION_ROUTINE callback function [Files]","_win32_fileiocompletionroutine","base.fileiocompletionroutine","fs.fileiocompletionroutine","minwinbase/FileIOCompletionRoutine","minwinbase/LPOVERLAPPED_COMPLETION_ROUTINE"]
old-location: fs\fileiocompletionroutine.htm
tech.root: fs
ms.assetid: 574eccda-03eb-4e8a-9d74-cfaecc7312ce
ms.date: 12/05/2018
ms.keywords: FileIOCompletionRoutine, FileIOCompletionRoutine callback, FileIOCompletionRoutine callback function [Files], LPOVERLAPPED_COMPLETION_ROUTINE, LPOVERLAPPED_COMPLETION_ROUTINE callback function [Files], _win32_fileiocompletionroutine, base.fileiocompletionroutine, fs.fileiocompletionroutine, minwinbase/FileIOCompletionRoutine, minwinbase/LPOVERLAPPED_COMPLETION_ROUTINE
req.header: minwinbase.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPOVERLAPPED_COMPLETION_ROUTINE
 - minwinbase/LPOVERLAPPED_COMPLETION_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - minwinbase.h
api_name:
 - FileIOCompletionRoutine
 - LPOVERLAPPED_COMPLETION_ROUTINE
---

## -description

An application-defined callback function used with the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a> and 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a> functions. It is called when the asynchronous 
    input and output (I/O) operation is completed or canceled and the calling thread is in an alertable 
    state (by using the <a href="/windows/desktop/api/synchapi/nf-synchapi-sleepex">SleepEx</a>, 
    <a href="/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex">MsgWaitForMultipleObjectsEx</a>, 
    <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex">WaitForSingleObjectEx</a>, or 
    <a href="/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex">WaitForMultipleObjectsEx</a> function with the 
    <i>fAlertable</i> parameter set to <b>TRUE</b>).

The <b>LPOVERLAPPED_COMPLETION_ROUTINE</b> type defines a pointer to this callback 
    function. <b>FileIOCompletionRoutine</b> is a 
    placeholder for the application-defined function name.

## -parameters

### -param dwErrorCode [in]

The I/O completion status. This parameter can be one of the 
      <a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

### -param dwNumberOfBytesTransfered [in]

The number of bytes transferred. If an error occurs, this parameter is zero.

### -param lpOverlapped [in, out]

A pointer to the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure specified by 
       the asynchronous I/O function.

The system does not use the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure 
       after the completion routine is called, so the completion routine can deallocate the memory used by the 
       overlapped structure.

## -remarks

The return value for an asynchronous operation is 0 (<b>ERROR_SUCCESS</b>) if the operation 
    completed successfully or if the operation completed with a warning. To determine whether an I/O operation was 
    completed successfully, check that <i>dwErrorCode</i> is 0, call 
    <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>, then call 
    <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. For example, if the buffer was not large 
    enough to receive all of the data from a call to <a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a>, 
    <i>dwErrorCode</i> is set to 0, 
    <b>GetOverlappedResult</b> fails, and 
    <b>GetLastError</b> returns 
    <b>ERROR_MORE_DATA</b>.

Returning from this function allows another pending I/O completion routine to be called. All waiting 
    completion routines are called before the alertable thread's wait is completed with a return code of 
    <b>WAIT_IO_COMPLETION</b>. The system may call the waiting completion routines in any order. 
    They may or may not be called in the order the I/O functions are completed.

Each time the system calls a completion routine, it uses some of the application's stack. If the completion 
    routine does additional asynchronous I/O and alertable waits, the stack may grow.

For more information, see 
    <a href="/windows/desktop/Sync/asynchronous-procedure-calls">Asynchronous Procedure Calls</a>.


## Examples

For  example code, see 
     <a href="/windows/desktop/ipc/named-pipe-server-using-completion-routines">Named Pipe Server Using Completion Routines</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-bindiocompletioncallback">BindIoCompletionCallback</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-sleepex">SleepEx</a>



<a href="/windows/desktop/FileIO/synchronous-and-asynchronous-i-o">Synchronous and Asynchronous I/O</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex">WaitForMultipleObjectsEx</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex">WaitForSingleObjectEx</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a>
