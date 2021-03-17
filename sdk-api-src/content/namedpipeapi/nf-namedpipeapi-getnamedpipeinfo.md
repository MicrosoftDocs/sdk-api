---
UID: NF:namedpipeapi.GetNamedPipeInfo
title: GetNamedPipeInfo function (namedpipeapi.h)
description: Retrieves information about the specified named pipe.
helpviewer_keywords: ["GetNamedPipeInfo","GetNamedPipeInfo function","PIPE_CLIENT_END","PIPE_SERVER_END","PIPE_TYPE_BYTE","PIPE_TYPE_MESSAGE","_win32_getnamedpipeinfo","base.getnamedpipeinfo","namedpipeapi/GetNamedPipeInfo"]
old-location: base\getnamedpipeinfo.htm
tech.root: base
ms.assetid: 91081373-60cd-4a90-a304-1e67fff9a483
ms.date: 12/05/2018
ms.keywords: GetNamedPipeInfo, GetNamedPipeInfo function, PIPE_CLIENT_END, PIPE_SERVER_END, PIPE_TYPE_BYTE, PIPE_TYPE_MESSAGE, _win32_getnamedpipeinfo, base.getnamedpipeinfo, namedpipeapi/GetNamedPipeInfo
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
 - GetNamedPipeInfo
 - namedpipeapi/GetNamedPipeInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-NamedPipe-l1-2-1.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-NamedPipe-L1-2-2.dll
api_name:
 - GetNamedPipeInfo
---

# GetNamedPipeInfo function


## -description

Retrieves information about the specified named pipe.

## -parameters

### -param hNamedPipe [in]

A handle to the named pipe instance. The handle must have GENERIC_READ access to the named pipe for a read-only or read/write pipe, or it must have GENERIC_WRITE and FILE_READ_ATTRIBUTES access for a write-only pipe. 




This parameter can also be a handle to an anonymous pipe, as returned by the 
<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe">CreatePipe</a> function.

### -param lpFlags [out, optional]

A pointer to a variable that receives the type of the named pipe. This parameter can be <b>NULL</b> if this information is not required. Otherwise, this parameter can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PIPE_CLIENT_END"></a><a id="pipe_client_end"></a><dl>
<dt><b>PIPE_CLIENT_END</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The handle refers to the client end of a named pipe instance. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="PIPE_SERVER_END"></a><a id="pipe_server_end"></a><dl>
<dt><b>PIPE_SERVER_END</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The handle refers to the server end of a named pipe instance. If this value is not specified, the handle refers to the client end of a named pipe instance.

</td>
</tr>
<tr>
<td width="40%"><a id="PIPE_TYPE_BYTE"></a><a id="pipe_type_byte"></a><dl>
<dt><b>PIPE_TYPE_BYTE</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The named pipe is a byte pipe. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="PIPE_TYPE_MESSAGE"></a><a id="pipe_type_message"></a><dl>
<dt><b>PIPE_TYPE_MESSAGE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The named pipe is a message pipe. If this value is not specified, the pipe is a byte pipe.

</td>
</tr>
</table>

### -param lpOutBufferSize [out, optional]

A pointer to a variable that receives the size of the buffer for outgoing data, in bytes. If the buffer size is zero, the buffer is allocated as needed. This parameter can be <b>NULL</b> if this information is not required.

### -param lpInBufferSize [out, optional]

A pointer to a variable that receives the size of the buffer for incoming data, in bytes. If the buffer size is zero, the buffer is allocated as needed. This parameter can be <b>NULL</b> if this information is not required.

### -param lpMaxInstances [out, optional]

A pointer to a variable that receives the maximum number of pipe instances that can be created. If the variable is set to PIPE_UNLIMITED_INSTANCES (255), the number of pipe instances that can be created is limited only by the availability of system resources. This parameter can be <b>NULL</b> if this information is not required.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax "\\\\.\\pipe\\LOCAL\\" for the pipe name.

## -see-also

<a href="/windows/win32/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a>



<a href="/windows/win32/api/winbase/nf-winbase-getnamedpipehandlestatea">GetNamedPipeHandleState</a>



<a href="/windows/win32/ipc/pipe-functions">Pipe Functions</a>



<a href="/windows/win32/ipc/pipes">Pipes Overview</a>

