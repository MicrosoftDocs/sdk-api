---
UID: NF:namedpipeapi.PeekNamedPipe
title: PeekNamedPipe function (namedpipeapi.h)
description: Copies data from a named or anonymous pipe into a buffer without removing it from the pipe.
helpviewer_keywords: ["PeekNamedPipe","PeekNamedPipe function","_win32_peeknamedpipe","base.peeknamedpipe","namedpipeapi/PeekNamedPipe"]
old-location: base\peeknamedpipe.htm
tech.root: base
ms.assetid: 125e0fbb-9013-4194-bc0b-1b8ea7db799e
ms.date: 12/05/2018
ms.keywords: PeekNamedPipe, PeekNamedPipe function, _win32_peeknamedpipe, base.peeknamedpipe, namedpipeapi/PeekNamedPipe
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
 - PeekNamedPipe
 - namedpipeapi/PeekNamedPipe
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
 - PeekNamedPipe
---

# PeekNamedPipe function


## -description

Copies data from a named or anonymous pipe into a buffer without removing it from the pipe. It also returns information about data in the pipe.

## -parameters

### -param hNamedPipe [in]

A handle to the pipe. This parameter can be a handle to a named pipe instance, as returned by the 
<a href="/windows/win32/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> or 
<a href="/windows/win32/api/fileapi/nf-fileapi-createfilew">CreateFile</a> function, or it can be a handle to the read end of an anonymous pipe, as returned by the 
<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe">CreatePipe</a> function. The handle must have GENERIC_READ access to the pipe.

### -param lpBuffer [out, optional]

A pointer to a buffer that receives data read from the pipe. This parameter can be <b>NULL</b> if no data is to be read.

### -param nBufferSize [in]

The size of the buffer specified by the <i>lpBuffer</i> parameter, in bytes. This parameter is ignored if <i>lpBuffer</i> is <b>NULL</b>.

### -param lpBytesRead [out, optional]

A pointer to a variable that receives the number of bytes read from the pipe. This parameter can be <b>NULL</b> if no data is to be read.

### -param lpTotalBytesAvail [out, optional]

A pointer to a variable that receives the total number of bytes available to be read from the pipe. This parameter can be <b>NULL</b> if no data is to be read.

### -param lpBytesLeftThisMessage [out, optional]

A pointer to a variable that receives the number of bytes remaining in this message. This parameter will be zero for byte-type named pipes or for anonymous pipes. This parameter can be <b>NULL</b> if no data is to be read.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>PeekNamedPipe</b> function is similar to the 
<a href="/windows/win32/api/fileapi/nf-fileapi-readfile">ReadFile</a> function with the following exceptions:

<ul>
<li>The data is read in the mode specified with 
<a href="/windows/win32/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a>. For example, create a pipe with PIPE_TYPE_MESSAGE | PIPE_READMODE_MESSAGE. If you change the mode to PIPE_READMODE_BYTE with 
<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate">SetNamedPipeHandleState</a>, <a href="/windows/win32/api/fileapi/nf-fileapi-readfile">ReadFile</a> will read in byte mode, but 
<b>PeekNamedPipe</b> will continue to read in message mode.</li>
<li>The data read from the pipe is not removed from the pipe's buffer.</li>
<li>The function can return additional information about the contents of the pipe.</li>
<li>The function always returns immediately in a single-threaded application, even if there is no data in the pipe. The wait mode of a named pipe handle (blocking or nonblocking) has no effect on the function.</li>
</ul>
<div class="alert"><b>Note</b>  The <b>PeekNamedPipe</b> function can block thread execution the same way any I/O function can when called on a synchronous handle in a multi-threaded application. To avoid this condition, use a pipe handle created for <a href="/windows/win32/FileIO/synchronous-and-asynchronous-i-o">asynchronous I/O</a>.</div>
<div> </div>
If the specified handle is a named pipe handle in byte-read mode, the function reads all available bytes up to the size specified in <i>nBufferSize</i>. For a named pipe handle in message-read mode, the function reads the next message in the pipe. If the message is larger than <i>nBufferSize</i>, the function returns <b>TRUE</b> after reading the specified number of bytes. In this situation, <i>lpBytesLeftThisMessage</i> will receive the number of bytes remaining in the message.

<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax `\\.\pipe\LOCAL\` for the pipe name.

## -see-also

<a href="/windows/win32/api/fileapi/nf-fileapi-createfilew">CreateFile</a>



<a href="/windows/win32/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a>



<a href="/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe">CreatePipe</a>



<a href="/windows/win32/ipc/pipe-functions">Pipe Functions</a>



<a href="/windows/win32/ipc/pipes">Pipes Overview</a>



<a href="/windows/win32/api/fileapi/nf-fileapi-readfile">ReadFile</a>



<a href="/windows/win32/api/fileapi/nf-fileapi-writefile">WriteFile</a>

