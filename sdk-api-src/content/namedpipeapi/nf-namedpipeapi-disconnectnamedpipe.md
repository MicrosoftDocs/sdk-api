---
UID: NF:namedpipeapi.DisconnectNamedPipe
title: DisconnectNamedPipe function (namedpipeapi.h)
description: Disconnects the server end of a named pipe instance from a client process.
helpviewer_keywords: ["DisconnectNamedPipe","DisconnectNamedPipe function","_win32_disconnectnamedpipe","base.disconnectnamedpipe","namedpipeapi/DisconnectNamedPipe"]
old-location: base\disconnectnamedpipe.htm
tech.root: base
ms.assetid: 7af2d4fa-5e19-4256-a713-ac5bdaee6023
ms.date: 12/05/2018
ms.keywords: DisconnectNamedPipe, DisconnectNamedPipe function, _win32_disconnectnamedpipe, base.disconnectnamedpipe, namedpipeapi/DisconnectNamedPipe
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
 - DisconnectNamedPipe
 - namedpipeapi/DisconnectNamedPipe
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
 - DisconnectNamedPipe
---

# DisconnectNamedPipe function


## -description

Disconnects the server end of a named pipe instance from a client process.

## -parameters

### -param hNamedPipe [in]

A handle to an instance of a named pipe. This handle must be created by the 
<a href="/windows/win32/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the client end of the named pipe is open, the 
<b>DisconnectNamedPipe</b> function forces that end of the named pipe closed. The client receives an error the next time it attempts to access the pipe. A client that is forced off a pipe by 
<b>DisconnectNamedPipe</b> must still use the <a href="/windows/win32/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close its end of the pipe.

The pipe exists as long as a server or client process has an open handle to the pipe.

When the server process disconnects a pipe instance, any unread data in the pipe is discarded. Before disconnecting, the server can make sure data is not lost by calling the <a href="/windows/win32/api/fileapi/nf-fileapi-flushfilebuffers">FlushFileBuffers</a> function, which does not return until the client process has read all the data.

The server process must call 
<b>DisconnectNamedPipe</b> to disconnect a pipe handle from its previous client before the handle can be connected to another client by using the 
<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe">ConnectNamedPipe</a> function.

<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax `\\.\pipe\LOCAL\` for the pipe name.


#### Examples

For an example, see 
<a href="/windows/win32/ipc/multithreaded-pipe-server">Multithreaded Pipe Server</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe">ConnectNamedPipe</a>



<a href="/windows/win32/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a>



<a href="/windows/win32/api/fileapi/nf-fileapi-flushfilebuffers">FlushFileBuffers</a>



<a href="/windows/win32/ipc/pipe-functions">Pipe Functions</a>



<a href="/windows/win32/ipc/pipes">Pipes Overview</a>

