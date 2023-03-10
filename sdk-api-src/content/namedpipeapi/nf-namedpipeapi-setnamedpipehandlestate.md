---
UID: NF:namedpipeapi.SetNamedPipeHandleState
title: SetNamedPipeHandleState function (namedpipeapi.h)
description: Sets the read mode and the blocking mode of the specified named pipe. If the specified handle is to the client end of a named pipe and if the named pipe server process is on a remote computer, the function can also be used to control local buffering.
helpviewer_keywords: ["PIPE_NOWAIT","PIPE_READMODE_BYTE","PIPE_READMODE_MESSAGE","PIPE_WAIT","SetNamedPipeHandleState","SetNamedPipeHandleState function","_win32_setnamedpipehandlestate","base.setnamedpipehandlestate","namedpipeapi/SetNamedPipeHandleState"]
old-location: base\setnamedpipehandlestate.htm
tech.root: base
ms.assetid: 1e62c98e-cecb-4f42-9269-e58ca69e5d39
ms.date: 12/05/2018
ms.keywords: PIPE_NOWAIT, PIPE_READMODE_BYTE, PIPE_READMODE_MESSAGE, PIPE_WAIT, SetNamedPipeHandleState, SetNamedPipeHandleState function, _win32_setnamedpipehandlestate, base.setnamedpipehandlestate, namedpipeapi/SetNamedPipeHandleState
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
 - SetNamedPipeHandleState
 - namedpipeapi/SetNamedPipeHandleState
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
 - SetNamedPipeHandleState
---

# SetNamedPipeHandleState function


## -description

Sets the read mode and the blocking mode of the specified named pipe. If the specified handle is to the client end of a named pipe and if the named pipe server process is on a remote computer, the function can also be used to control local buffering.

## -parameters

### -param hNamedPipe [in]

 A handle to the named pipe instance. This parameter can be a handle to the server end of the pipe, as returned by the 
<a href="/windows/win32/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> function, or to the client end of the pipe, as returned by the 
<a href="/windows/win32/api/fileapi/nf-fileapi-createfilew">CreateFile</a> function. The handle must have GENERIC_WRITE access to the named pipe for a write-only or read/write pipe, or it must have GENERIC_READ and FILE_WRITE_ATTRIBUTES access for a read-only pipe. 




This parameter can also be a handle to an anonymous pipe, as returned by the 
<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe">CreatePipe</a> function.

### -param lpMode [in, optional]

The new pipe mode. The mode is a combination of a read-mode flag and a wait-mode flag. This parameter can be <b>NULL</b> if the mode is not being set. Specify one of the following modes. 



<table>
<tr>
<th>Mode</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PIPE_READMODE_BYTE"></a><a id="pipe_readmode_byte"></a><dl>
<dt><b>PIPE_READMODE_BYTE</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Data is read from the pipe as a stream of bytes. This mode is the default if no read-mode flag is specified.

</td>
</tr>
<tr>
<td width="40%"><a id="PIPE_READMODE_MESSAGE"></a><a id="pipe_readmode_message"></a><dl>
<dt><b>PIPE_READMODE_MESSAGE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Data is read from the pipe as a stream of messages. The function fails if this flag is specified for a byte-type pipe.

</td>
</tr>
</table>
 

One of the following wait modes can be specified.

<table>
<tr>
<th>Mode</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PIPE_WAIT"></a><a id="pipe_wait"></a><dl>
<dt><b>PIPE_WAIT</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Blocking mode is enabled. This mode is the default if no wait-mode flag is specified. When a blocking mode pipe handle is specified in the 
<a href="/windows/win32/api/fileapi/nf-fileapi-readfile">ReadFile</a>, 
<a href="/windows/win32/api/fileapi/nf-fileapi-writefile">WriteFile</a>, or 
<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe">ConnectNamedPipe</a> function, operations are not finished until there is data to read, all data is written, or a client is connected. Use of this mode can mean waiting indefinitely in some situations for a client process to perform an action.

</td>
</tr>
<tr>
<td width="40%"><a id="PIPE_NOWAIT"></a><a id="pipe_nowait"></a><dl>
<dt><b>PIPE_NOWAIT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Nonblocking mode is enabled. In this mode, <a href="/windows/win32/api/fileapi/nf-fileapi-readfile">ReadFile</a>, <a href="/windows/win32/api/fileapi/nf-fileapi-writefile">WriteFile</a>, and 
<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe">ConnectNamedPipe</a> always return immediately. Note that nonblocking mode is supported for compatibility with Microsoft LAN Manager version 2.0 and should not be used to achieve asynchronous input and output (I/O) with named pipes.

</td>
</tr>
</table>

### -param lpMaxCollectionCount [in, optional]

The maximum number of bytes collected on the client computer before transmission to the server. This parameter must be <b>NULL</b> if the specified pipe handle is to the server end of a named pipe or if client and server processes are on the same machine. This parameter is ignored if the client process specifies the FILE_FLAG_WRITE_THROUGH flag in the <a href="/windows/win32/api/fileapi/nf-fileapi-createfilew">CreateFile</a> function when the handle was created. This parameter can be <b>NULL</b> if the collection count is not being set.

### -param lpCollectDataTimeout [in, optional]

The maximum time, in milliseconds, that can pass before a remote named pipe transfers information over the network. This parameter must be <b>NULL</b> if the specified pipe handle is to the server end of a named pipe or if client and server processes are on the same computer. This parameter is ignored if the client process specified the FILE_FLAG_WRITE_THROUGH flag in the 
<a href="/windows/win32/api/fileapi/nf-fileapi-createfilew">CreateFile</a> function when the handle was created. This parameter can be <b>NULL</b> if the collection count is not being set.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax `\\.\pipe\LOCAL\` for the pipe name.


#### Examples

For an example, see 
<a href="/windows/win32/ipc/named-pipe-client">Named Pipe Client</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe">ConnectNamedPipe</a>



<a href="/windows/win32/api/fileapi/nf-fileapi-createfilew">CreateFile</a>



<a href="/windows/win32/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a>



<a href="/windows/win32/api/winbase/nf-winbase-getnamedpipehandlestatea">GetNamedPipeHandleState</a>



<a href="/windows/win32/ipc/pipe-functions">Pipe Functions</a>



<a href="/windows/win32/ipc/pipes">Pipes Overview</a>



<a href="/windows/win32/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/win32/api/fileapi/nf-fileapi-writefile">WriteFile</a>

