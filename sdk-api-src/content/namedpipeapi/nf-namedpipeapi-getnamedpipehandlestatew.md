---
UID: NF:namedpipeapi.GetNamedPipeHandleStateW
tech.root: base 
title: GetNamedPipeHandleStateW
ms.date: 08/05/2022
targetos: Windows
description: The GetNamedPipeHandleStateW (Unicode) function (winbase.h) retrieves information about a specified named pipe. 
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Kernel32.dll 
req.header: namedpipeapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Kernel32.lib 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps] 
req.target-type: Windows 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-Ms-Win-Core-NamedPipe-Ansi-L1-1-0.dll
 - API-Ms-Win-Core-NamedPipe-L1-2-1.dll
 - Kernel32Legacy.dll
 - KernelBase.dll
 - API-MS-Win-Core-NamedPipe-Ansi-L1-1-1.dll
 - API-MS-Win-Core-NamedPipe-L1-2-2.dll
api_name:
 - GetNamedPipeHandleStateW
 - GetNamedPipeHandleState
f1_keywords:
 - GetNamedPipeHandleStateW
 - namedpipeapi/GetNamedPipeHandleStateW
 - GetNamedPipeHandleState
 - namedpipeapi/GetNamedPipeHandleState
dev_langs:
 - c++
---

# GetNamedPipeHandleStateW function

## -description

Retrieves information about a specified named pipe. The information returned can vary during the lifetime of an instance of the named pipe.

## -parameters

### -param hNamedPipe [in]

A handle to the named pipe for which information is wanted. The handle must have GENERIC_READ access for a read-only or read/write pipe, or it must have GENERIC_WRITE and FILE_READ_ATTRIBUTES access for a write-only pipe.  

This parameter can also be a handle to an anonymous pipe, as returned by the 
<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-createpipe">CreatePipe</a> function.

### -param lpState [out, optional]

A pointer to a variable that indicates the current state of the handle. This parameter can be <b>NULL</b> if this information is not needed. Either or both of the following values can be specified.  

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PIPE_NOWAIT"></a><a id="pipe_nowait"></a><dl>
<dt><b>PIPE_NOWAIT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The pipe handle is in nonblocking mode. If this flag is not specified, the pipe handle is in blocking mode.

</td>
</tr>
<tr>
<td width="40%"><a id="PIPE_READMODE_MESSAGE"></a><a id="pipe_readmode_message"></a><dl>
<dt><b>PIPE_READMODE_MESSAGE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The pipe handle is in message-read mode. If this flag is not specified, the pipe handle is in byte-read mode.

</td>
</tr>
</table>

### -param lpCurInstances [out, optional]

A pointer to a variable that receives the number of current pipe instances. This parameter can be <b>NULL</b> if this information is not required.

### -param lpMaxCollectionCount [out, optional]

A pointer to a variable that receives the maximum number of bytes to be collected on the client's computer before transmission to the server. This parameter must be <b>NULL</b> if the specified pipe handle is to the server end of a named pipe or if client and server processes are on the same computer. This parameter can be <b>NULL</b> if this information is not required.

### -param lpCollectDataTimeout [out, optional]

A pointer to a variable that receives the maximum time, in milliseconds, that can pass before a remote named pipe transfers information over the network. This parameter must be <b>NULL</b> if the specified pipe handle is to the server end of a named pipe or if client and server processes are on the same computer. This parameter can be <b>NULL</b> if this information is not required.

### -param lpUserName [out, optional]

A pointer to a buffer that receives the user name string associated with the client application. The server can only retrieve this information if the client opened the pipe with SECURITY_IMPERSONATION access.

This parameter must be <b>NULL</b> if the specified pipe handle is to the client end of a named pipe. This parameter can be <b>NULL</b> if this information is not required.

### -param nMaxUserNameSize [in]

The size of the buffer specified by the <i>lpUserName</i> parameter, in <b>TCHARs</b>. This parameter is ignored if <i>lpUserName</i> is <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>GetNamedPipeHandleState</b> function returns successfully even if all of the pointers passed to it are <b>NULL</b>.

To set the pipe handle state, use the 
<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate">SetNamedPipeHandleState</a> function.

<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax `\\.\pipe\LOCAL\` for the pipe name.

## -see-also

<a href="/windows/desktop/ipc/pipe-functions">Pipe Functions</a>  
<a href="/windows/desktop/ipc/pipes">Pipes Overview</a>  
<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate">SetNamedPipeHandleState</a>  
