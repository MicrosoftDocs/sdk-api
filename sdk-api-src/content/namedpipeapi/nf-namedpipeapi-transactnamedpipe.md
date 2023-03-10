---
UID: NF:namedpipeapi.TransactNamedPipe
title: TransactNamedPipe function (namedpipeapi.h)
description: Combines the functions that write a message to and read a message from the specified named pipe into a single operation.
helpviewer_keywords: ["TransactNamedPipe","TransactNamedPipe function","_win32_transactnamedpipe","base.transactnamedpipe","namedpipeapi/TransactNamedPipe"]
old-location: base\transactnamedpipe.htm
tech.root: base
ms.assetid: 79afcb18-babb-453e-8618-81b43ecb24c4
ms.date: 12/05/2018
ms.keywords: TransactNamedPipe, TransactNamedPipe function, _win32_transactnamedpipe, base.transactnamedpipe, namedpipeapi/TransactNamedPipe
req.header: namedpipeapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - TransactNamedPipe
 - namedpipeapi/TransactNamedPipe
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-NamedPipe-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-NamedPipe-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-NamedPipe-l1-2-1.dll
 - API-MS-Win-Core-NamedPipe-L1-2-2.dll
api_name:
 - TransactNamedPipe
---

# TransactNamedPipe function


## -description

Combines the functions that write a message to and read a message from the specified named pipe into a single operation.

## -parameters

### -param hNamedPipe [in]

A handle to the named pipe returned by the 
<a href="/windows/win32/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> or 
<a href="/windows/win32/api/fileapi/nf-fileapi-createfilew">CreateFile</a> function. 




This parameter can also be a handle to an anonymous pipe, as returned by the 
<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe">CreatePipe</a> function.

### -param lpInBuffer [in]

A pointer to the buffer containing the data to be written to the pipe.

### -param nInBufferSize [in]

The size of the input buffer, in bytes.

### -param lpOutBuffer [out]

A pointer to the buffer that receives the data read from the pipe.

### -param nOutBufferSize [in]

The size of the output buffer, in bytes.

### -param lpBytesRead [out]

A pointer to the variable that receives the number of bytes read from the pipe. 




If <i>lpOverlapped</i> is <b>NULL</b>, <i>lpBytesRead</i> cannot be <b>NULL</b>.

If <i>lpOverlapped</i> is not <b>NULL</b>, <i>lpBytesRead</i> can be <b>NULL</b>. If this is an overlapped read operation, you can get the number of bytes read by calling 
<a href="/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>. If <i>hNamedPipe</i> is associated with an I/O completion port, you can get the number of bytes read by calling 
<a href="/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>.

### -param lpOverlapped [in, out, optional]

A pointer to an 
<a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. This structure is required if <i>hNamedPipe</i> was opened with FILE_FLAG_OVERLAPPED. 




If <i>hNamedPipe</i> was opened with FILE_FLAG_OVERLAPPED, the <i>lpOverlapped</i> parameter must not be <b>NULL</b>. It must point to a valid <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. If <i>hNamedPipe</i> was created with FILE_FLAG_OVERLAPPED and <i>lpOverlapped</i> is <b>NULL</b>, the function can incorrectly report that the operation is complete.

If <i>hNamedPipe</i> was opened with FILE_FLAG_OVERLAPPED and <i>lpOverlapped</i> is not <b>NULL</b>, 
<b>TransactNamedPipe</b> is executed as an overlapped operation. The <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure should contain a manual-reset event object (which can be created by using the 
<a href="/windows/win32/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function). If the operation cannot be completed immediately, 
<b>TransactNamedPipe</b> returns <b>FALSE</b> and <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_IO_PENDING. In this situation, the event object is set to the nonsignaled state before 
<b>TransactNamedPipe</b> returns, and it is set to the signaled state when the transaction has finished. Also, you can  be notified when an overlapped operation completes by using the <a href="/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a> or <a href="/windows/win32/FileIO/getqueuedcompletionstatusex-func">GetQueuedCompletionStatusEx</a> functions.  In this case, you do not need to assign the manual-reset event in the <b>OVERLAPPED</b> structure, and the completion happens against <i>hNamedPipe</i> in the same way as an asynchronous read or write operation. For more information about overlapped operations, see 
<a href="/windows/win32/ipc/pipes">Pipes</a>.

If <i>hNamedPipe</i> was not opened with FILE_FLAG_OVERLAPPED, 
<b>TransactNamedPipe</b> does not return until the operation is complete.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the message to be read is longer than the buffer specified by the <i>nOutBufferSize</i> parameter, 
<b>TransactNamedPipe</b> returns <b>FALSE</b> and the <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns ERROR_MORE_DATA. The remainder of the message can be read by a subsequent call to <a href="/windows/win32/api/fileapi/nf-fileapi-readfile">ReadFile</a>, <a href="/windows/win32/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a>, or 
<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe">PeekNamedPipe</a>.

## -remarks

<b>TransactNamedPipe</b> fails if the server did not create the pipe as a message-type pipe or if the pipe handle is not in message-read mode. For example, if a client is running on the same machine as the server and uses the \\.\pipe&#92;<i>pipename</i> format to open the pipe, the pipe is opened in byte mode by the named pipe file system (NPFS). If the client uses the form &#92;&#92;<i>server</i>\pipe&#92;<i>pipename</i>, the redirector opens the pipe in message mode. A byte mode pipe handle can be changed to message-read mode with the 
<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate">SetNamedPipeHandleState</a> function.

The function cannot be completed successfully until data is written into the buffer specified by the <i>lpOutBuffer</i> parameter. The <i>lpOverlapped</i> parameter is available to enable the calling thread to perform other tasks while the operation is executing in the background.

The maximum guaranteed size of a named pipe transaction is 64 kilobytes. In some limited cases, transactions beyond 64 kilobytes are possible, depending on OS versions participating in the transaction and dynamic network conditions. However, there is no guarantee that transactions above 64 kilobytes will succeed. Therefore it's recommended that named pipe transactions be limited to 64 kilobytes of data.

<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax `\\.\pipe\LOCAL\` for the pipe name.


#### Examples

For an example, see 
<a href="/windows/win32/ipc/transactions-on-named-pipes">Transactions on Named Pipes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/win32/api/fileapi/nf-fileapi-createfilew">CreateFile</a>



<a href="/windows/win32/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a>



<a href="/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>



<a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe">PeekNamedPipe</a>



<a href="/windows/win32/ipc/pipe-functions">Pipe Functions</a>



<a href="/windows/win32/ipc/pipes">Pipes Overview</a>



<a href="/windows/win32/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/win32/api/fileapi/nf-fileapi-readfileex">ReadFileEx</a>



<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate">SetNamedPipeHandleState</a>

