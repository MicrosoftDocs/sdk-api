---
UID: NF:namedpipeapi.ConnectNamedPipe
title: ConnectNamedPipe function (namedpipeapi.h)
description: Enables a named pipe server process to wait for a client process to connect to an instance of a named pipe.
helpviewer_keywords: ["ConnectNamedPipe","ConnectNamedPipe function","_win32_connectnamedpipe","base.connectnamedpipe","namedpipeapi/ConnectNamedPipe"]
old-location: base\connectnamedpipe.htm
tech.root: base
ms.assetid: 50f6680f-900e-4411-a849-ec9a911c9e32
ms.date: 12/05/2018
ms.keywords: ConnectNamedPipe, ConnectNamedPipe function, _win32_connectnamedpipe, base.connectnamedpipe, namedpipeapi/ConnectNamedPipe
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
 - ConnectNamedPipe
 - namedpipeapi/ConnectNamedPipe
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
 - ConnectNamedPipe
---

# ConnectNamedPipe function


## -description

Enables a named pipe server process to wait for a client process to connect to an instance of a named pipe. A client process connects by calling either the 
<a href="/windows/win32/api/fileapi/nf-fileapi-createfilew">CreateFile</a> or 
<a href="/windows/win32/api/winbase/nf-winbase-callnamedpipea">CallNamedPipe</a> function.

## -parameters

### -param hNamedPipe [in]

A handle to the server end of a named pipe instance. This handle is returned by the 
<a href="/windows/win32/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> function.

### -param lpOverlapped [in, out, optional]

A pointer to an 
<a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. 




If <i>hNamedPipe</i> was opened with FILE_FLAG_OVERLAPPED, the <i>lpOverlapped</i> parameter must not be <b>NULL</b>. It must point to a valid <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. If <i>hNamedPipe</i> was opened with FILE_FLAG_OVERLAPPED and <i>lpOverlapped</i> is <b>NULL</b>, the function can incorrectly report that the connect operation is complete.

If <i>hNamedPipe</i> was created with FILE_FLAG_OVERLAPPED and <i>lpOverlapped</i> is not <b>NULL</b>, the <a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure should  contain a handle to a manual-reset event object (which the server can create by using the 
<a href="/windows/win32/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function).

If <i>hNamedPipe</i> was not opened with FILE_FLAG_OVERLAPPED, the function does not return until a client is connected or an error occurs. Successful synchronous operations result in the function returning a nonzero value if a client connects after the function is called.

## -returns

If the operation is synchronous, <b>ConnectNamedPipe</b> does not return until the operation has completed. If the function succeeds, the return value is nonzero. If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the operation is asynchronous, <b>ConnectNamedPipe</b> returns immediately. If the operation is still pending, the return value is zero and <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_IO_PENDING. (You can use the <a href="/windows/win32/api/winbase/nf-winbase-hasoverlappediocompleted">HasOverlappedIoCompleted</a> macro to determine when the operation has finished.) If the function fails, the return value is zero and 
<b>GetLastError</b> returns a value other than ERROR_IO_PENDING or ERROR_PIPE_CONNECTED.

If a client connects before the function is called, the function returns zero and <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_PIPE_CONNECTED. This can happen if a client connects in the interval between the call to 
<a href="/windows/win32/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> and the call to 
<b>ConnectNamedPipe</b>. In this situation, there is a good connection between client and server, even though the function returns zero.

## -remarks

A named pipe server process can use 
<b>ConnectNamedPipe</b> with a newly created pipe instance. It can also be used with an instance that was previously connected to another client process; in this case, the server process must first call the 
<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe">DisconnectNamedPipe</a> function to disconnect the handle from the previous client before the handle can be reconnected to a new client. Otherwise, 
<b>ConnectNamedPipe</b> returns zero, and <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_NO_DATA if the previous client has closed its handle or ERROR_PIPE_CONNECTED if it has not closed its handle.

The behavior of 
<b>ConnectNamedPipe</b> depends on two conditions: whether the pipe handle's wait mode is set to blocking or nonblocking and whether the function is set to execute synchronously or in overlapped mode. A server initially specifies a pipe handle's wait mode in the 
<a href="/windows/win32/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> function, and it can be changed by using the 
<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate">SetNamedPipeHandleState</a> function.

The server process can use any of the 
<a href="/windows/win32/Sync/wait-functions">wait functions</a> or 
<a href="/windows/win32/api/synchapi/nf-synchapi-sleepex">SleepEx</a>— to determine when the state of the event object is signaled, and it can then use the <a href="/windows/win32/api/winbase/nf-winbase-hasoverlappediocompleted">HasOverlappedIoCompleted</a> 
macro to determine when the 
<b>ConnectNamedPipe</b> operation completes.

If the specified pipe handle is in nonblocking mode, 
<b>ConnectNamedPipe</b> always returns immediately. In nonblocking mode, 
<b>ConnectNamedPipe</b> returns a nonzero value the first time it is called for a pipe instance that is disconnected from a previous client. This indicates that the pipe is now available to be connected to a new client process. In all other situations when the pipe handle is in nonblocking mode, 
<b>ConnectNamedPipe</b> returns zero. In these situations, <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_PIPE_LISTENING if no client is connected, ERROR_PIPE_CONNECTED if a client is connected, and ERROR_NO_DATA if a previous client has closed its pipe handle but the server has not disconnected. Note that a good connection between client and server exists only after the ERROR_PIPE_CONNECTED error is received.

<div class="alert"><b>Note</b>  Nonblocking mode is supported for compatibility with Microsoft LAN Manager version 2.0, and it should not be used to achieve asynchronous input and output (I/O) with named pipes.</div>
<div> </div>
<b>Windows 10, version 1709 and later:  </b>Pipes cannot be used to communicate between app-containers; ie, from one UWP process to another UWP process that's not part of the same app. Also, named pipes within app-containers must use the syntax `\\.\pipe\LOCAL\` for the pipe name.


#### Examples

For an example, see 
<a href="/windows/win32/ipc/multithreaded-pipe-server">Multithreaded Pipe Server</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/api/winbase/nf-winbase-callnamedpipea">CallNamedPipe</a>



<a href="/windows/win32/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/win32/api/fileapi/nf-fileapi-createfilew">CreateFile</a>



<a href="/windows/win32/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a>



<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe">DisconnectNamedPipe</a>



<a href="/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>



<a href="/windows/win32/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/win32/ipc/pipe-functions">Pipe Functions</a>



<a href="/windows/win32/ipc/pipes">Pipes Overview</a>



<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate">SetNamedPipeHandleState</a>



<a href="/windows/win32/api/synchapi/nf-synchapi-sleepex">SleepEx</a>

