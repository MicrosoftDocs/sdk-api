---
UID: NF:winbase.GetNamedPipeHandleStateA
title: GetNamedPipeHandleStateA function (winbase.h)
author: windows-sdk-content
description: Retrieves information about a specified named pipe.
old-location: base\getnamedpipehandlestate.htm
tech.root: ipc
ms.assetid: a28003f0-f488-4ac3-91bf-dd7c5e87ea66
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetNamedPipeHandleState, GetNamedPipeHandleState function, GetNamedPipeHandleStateA, GetNamedPipeHandleStateW, PIPE_NOWAIT, PIPE_READMODE_MESSAGE, _win32_getnamedpipehandlestate, base.getnamedpipehandlestate, winbase/GetNamedPipeHandleState, winbase/GetNamedPipeHandleStateA, winbase/GetNamedPipeHandleStateW
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetNamedPipeHandleStateW (Unicode) and GetNamedPipeHandleStateA (ANSI)
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
 - API-Ms-Win-Core-NamedPipe-Ansi-L1-1-0.dll
 - API-Ms-Win-Core-NamedPipe-L1-2-1.dll
 - Kernel32Legacy.dll
 - KernelBase.dll
 - API-MS-Win-Core-NamedPipe-Ansi-L1-1-1.dll
 - API-MS-Win-Core-NamedPipe-L1-2-2.dll
api_name:
 - GetNamedPipeHandleState
 - GetNamedPipeHandleStateA
 - GetNamedPipeHandleStateW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetNamedPipeHandleStateA function


## -description


Retrieves information about a specified named pipe. The information returned can vary during the lifetime of an instance of the named pipe.


## -parameters




### -param hNamedPipe [in]

A handle to the named pipe for which information is wanted. The handle must have GENERIC_READ access for a read-only or read/write pipe, or it must have GENERIC_WRITE and FILE_READ_ATTRIBUTES access for a write-only pipe. 




This parameter can also be a handle to an anonymous pipe, as returned by the 
<a href="https://msdn.microsoft.com/a2d2fee8-c174-49d3-9e5a-2ce3bb763932">CreatePipe</a> function.


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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>GetNamedPipeHandleState</b> function returns successfully even if all of the pointers passed to it are <b>NULL</b>.

To set the pipe handle state, use the 
<a href="https://msdn.microsoft.com/1e62c98e-cecb-4f42-9269-e58ca69e5d39">SetNamedPipeHandleState</a> function.

<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax "\\.\pipe\LOCAL\" for the pipe name.




## -see-also




<a href="https://msdn.microsoft.com/9e80783e-9641-4cbd-9c28-a8efe6b9efaa">Pipe Functions</a>



<a href="https://msdn.microsoft.com/7cb8cbe4-eec8-4dda-9cb7-8d37abcee6f4">Pipes Overview</a>



<a href="https://msdn.microsoft.com/1e62c98e-cecb-4f42-9269-e58ca69e5d39">SetNamedPipeHandleState</a>
 

 

