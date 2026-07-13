---
UID: NF:namedpipeapi.CreatePipe
title: CreatePipe function (namedpipeapi.h)
description: Creates an anonymous pipe, and returns handles to the read and write ends of the pipe.
helpviewer_keywords: ["CreatePipe","CreatePipe function","_win32_createpipe","base.createpipe","namedpipeapi/CreatePipe"]
old-location: base\createpipe.htm
tech.root: base
ms.assetid: a2d2fee8-c174-49d3-9e5a-2ce3bb763932
ms.date: 12/05/2018
ms.keywords: CreatePipe, CreatePipe function, _win32_createpipe, base.createpipe, namedpipeapi/CreatePipe
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
 - CreatePipe
 - namedpipeapi/CreatePipe
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
 - CreatePipe
---

# CreatePipe function


## -description

Creates an anonymous pipe, and returns handles to the read and write ends of the pipe.

## -parameters

### -param hReadPipe [out]

A pointer to a variable that receives the read handle for the pipe.

### -param hWritePipe [out]

A pointer to a variable that receives the write handle for the pipe.

### -param lpPipeAttributes [in, optional]

A pointer to a 
<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure that determines whether the returned handle can be inherited by child processes. If <i>lpPipeAttributes</i> is <b>NULL</b>, the handle cannot be inherited. 




The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the new pipe. If <i>lpPipeAttributes</i> is <b>NULL</b>, the pipe gets a default security descriptor. The ACLs in the default security descriptor for a pipe come from the primary or impersonation token of the creator.

### -param nSize [in]

The size of the buffer for the pipe, in bytes. The size is only a suggestion; the system uses the value to calculate an appropriate buffering mechanism. If this parameter is zero, the system uses the default buffer size.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>CreatePipe</b> creates the pipe, assigning the specified pipe size to the storage buffer. 
<b>CreatePipe</b> also creates handles that the process uses to read from and write to the buffer in subsequent calls to the <a href="/windows/win32/api/fileapi/nf-fileapi-readfile">ReadFile</a> and <a href="/windows/win32/api/fileapi/nf-fileapi-writefile">WriteFile</a> functions.

To read from the pipe, a process uses the read handle in a call to the <a href="/windows/win32/api/fileapi/nf-fileapi-readfile">ReadFile</a> function. <b>ReadFile</b> returns when one of the following is true: a write operation completes on the write end of the pipe, the number of bytes requested has been read, or an error occurs.

When a process uses <a href="/windows/win32/api/fileapi/nf-fileapi-writefile">WriteFile</a> to write to an anonymous pipe, the write operation is not completed until all bytes are written. If the pipe buffer is full before all bytes are written, <b>WriteFile</b> does not return until another process or thread uses <a href="/windows/win32/api/fileapi/nf-fileapi-readfile">ReadFile</a> to make more buffer space available.

Anonymous pipes are implemented using a named pipe with a unique name. Therefore, you can often pass a handle to an anonymous pipe to a function that requires a handle to a named pipe.

If <b>CreatePipe</b> fails, the contents of the output parameters are indeterminate. No assumptions should be made about their contents in this event.

To free resources used by a pipe, the application should always close handles when they are no longer needed, which is accomplished either by calling the <a href="/windows/win32/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function or when the process associated with the instance handles ends. Note that an instance of a pipe may have more than one handle associated with it. An instance of a pipe is always deleted when the last handle to the instance of the named pipe is closed.


#### Examples

For an example, see 
<a href="/windows/win32/ProcThread/creating-a-child-process-with-redirected-input-and-output">Creating a Child Process with Redirected Input and Output</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/ipc/pipe-functions">Pipe Functions</a>



<a href="/windows/win32/ipc/pipes">Pipes Overview</a>



<a href="/windows/win32/api/fileapi/nf-fileapi-readfile">ReadFile</a>


<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>


<a href="/windows/win32/api/fileapi/nf-fileapi-writefile">WriteFile</a>