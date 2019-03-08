---
UID: NF:namedpipeapi.DisconnectNamedPipe
title: DisconnectNamedPipe function
author: windows-sdk-content
description: Disconnects the server end of a named pipe instance from a client process.
old-location: base\disconnectnamedpipe.htm
tech.root: ipc
ms.assetid: 7af2d4fa-5e19-4256-a713-ac5bdaee6023
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DisconnectNamedPipe, DisconnectNamedPipe function, _win32_disconnectnamedpipe, base.disconnectnamedpipe, namedpipeapi/DisconnectNamedPipe
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DisconnectNamedPipe function


## -description


Disconnects the server end of a named pipe instance from a client process.


## -parameters




### -param hNamedPipe [in]

A handle to an instance of a named pipe. This handle must be created by the 
<a href="https://msdn.microsoft.com/00d79639-3f14-4964-90f3-9462a23e68df">CreateNamedPipe</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the client end of the named pipe is open, the 
<b>DisconnectNamedPipe</b> function forces that end of the named pipe closed. The client receives an error the next time it attempts to access the pipe. A client that is forced off a pipe by 
<b>DisconnectNamedPipe</b> must still use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close its end of the pipe.

The pipe exists as long as a server or client process has an open handle to the pipe.

When the server process disconnects a pipe instance, any unread data in the pipe is discarded. Before disconnecting, the server can make sure data is not lost by calling the <a href="base.flushfilebuffers">FlushFileBuffers</a> function, which does not return until the client process has read all the data.

The server process must call 
<b>DisconnectNamedPipe</b> to disconnect a pipe handle from its previous client before the handle can be connected to another client by using the 
<a href="https://msdn.microsoft.com/50f6680f-900e-4411-a849-ec9a911c9e32">ConnectNamedPipe</a> function.

<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax "\\.\pipe\LOCAL\" for the pipe name.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/4657e814-0e7f-45b5-8ddb-17ec0c3612ba">Multithreaded Pipe Server</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/50f6680f-900e-4411-a849-ec9a911c9e32">ConnectNamedPipe</a>



<a href="https://msdn.microsoft.com/00d79639-3f14-4964-90f3-9462a23e68df">CreateNamedPipe</a>



<a href="base.flushfilebuffers">FlushFileBuffers</a>



<a href="https://msdn.microsoft.com/9e80783e-9641-4cbd-9c28-a8efe6b9efaa">Pipe Functions</a>



<a href="https://msdn.microsoft.com/7cb8cbe4-eec8-4dda-9cb7-8d37abcee6f4">Pipes Overview</a>
 

 

