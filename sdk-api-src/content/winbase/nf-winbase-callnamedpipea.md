---
UID: NF:winbase.CallNamedPipeA
title: CallNamedPipeA function (winbase.h)
description: Connects to a message-type pipe (and waits if an instance of the pipe is not available), writes to and reads from the pipe, and then closes the pipe. (CallNamedPipeA)
helpviewer_keywords: ["CallNamedPipe","CallNamedPipe function","CallNamedPipeA","CallNamedPipeW","NMPWAIT_NOWAIT","NMPWAIT_USE_DEFAULT_WAIT","NMPWAIT_WAIT_FOREVER","_win32_callnamedpipe","base.callnamedpipe","winbase/CallNamedPipe","winbase/CallNamedPipeA","winbase/CallNamedPipeW"]
old-location: base\callnamedpipe.htm
tech.root: base
ms.assetid: 9cfcb608-a539-4eb6-866c-81dafdabbcdb
ms.date: 12/05/2018
ms.keywords: CallNamedPipe, CallNamedPipe function, CallNamedPipeA, CallNamedPipeW, NMPWAIT_NOWAIT, NMPWAIT_USE_DEFAULT_WAIT, NMPWAIT_WAIT_FOREVER, _win32_callnamedpipe, base.callnamedpipe, winbase/CallNamedPipe, winbase/CallNamedPipeA, winbase/CallNamedPipeW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CallNamedPipeW (Unicode) and CallNamedPipeA (ANSI)
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
 - CallNamedPipeA
 - winbase/CallNamedPipeA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-NamedPipe-Ansi-L1-1-1.dll
 - API-MS-Win-Core-NamedPipe-L1-2-2.dll
 - Kernel32Legacy.dll
 - KernelBase.dll
api_name:
 - CallNamedPipe
 - CallNamedPipeA
 - CallNamedPipeW
---

# CallNamedPipeA function


## -description

Connects to a message-type pipe (and waits if an instance of the pipe is not available), writes to and reads from the pipe, and then closes the pipe.

## -parameters

### -param lpNamedPipeName [in]

The pipe name.

### -param lpInBuffer [in]

The data to be written to the pipe.

### -param nInBufferSize [in]

The size of the write buffer, in bytes.

### -param lpOutBuffer [out]

A pointer to the buffer that receives the data read from the pipe.

### -param nOutBufferSize [in]

The size of the read buffer, in bytes.

### -param lpBytesRead [out]

A pointer to a variable that receives the number of bytes read from the pipe.

### -param nTimeOut [in]

The number of milliseconds to wait for the named pipe to be available. In addition to numeric values, the following special values can be specified.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NMPWAIT_NOWAIT"></a><a id="nmpwait_nowait"></a><dl>
<dt><b>NMPWAIT_NOWAIT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Does not wait for the named pipe. If the named pipe is not available, the function returns an error.

</td>
</tr>
<tr>
<td width="40%"><a id="NMPWAIT_WAIT_FOREVER"></a><a id="nmpwait_wait_forever"></a><dl>
<dt><b>NMPWAIT_WAIT_FOREVER</b></dt>
<dt>0xffffffff</dt>
</dl>
</td>
<td width="60%">
Waits indefinitely.

</td>
</tr>
<tr>
<td width="40%"><a id="NMPWAIT_USE_DEFAULT_WAIT"></a><a id="nmpwait_use_default_wait"></a><dl>
<dt><b>NMPWAIT_USE_DEFAULT_WAIT</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Uses the default time-out specified in a call to the 
<a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> function.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the message written to the pipe by the server process is longer than <i>nOutBufferSize</i>, 
<b>CallNamedPipe</b> returns <b>FALSE</b>, and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_MORE_DATA. The remainder of the message is discarded, because 
<b>CallNamedPipe</b> closes the handle to the pipe before returning.

## -remarks

Calling <b>CallNamedPipe</b> is equivalent to calling the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> (or <a href="/windows/desktop/api/winbase/nf-winbase-waitnamedpipea">WaitNamedPipe</a>, if <b>CreateFile</b> cannot open the pipe immediately), <a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe">TransactNamedPipe</a>, and <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> functions. <b>CreateFile</b> is called with an access flag of GENERIC_READ | GENERIC_WRITE, and an inherit handle flag of <b>FALSE</b>.

<b>CallNamedPipe</b> fails if the pipe is a byte-type pipe.

<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax `\\.\pipe\LOCAL\` for the pipe name.


#### Examples

For an example, see 
<a href="/windows/desktop/ipc/transactions-on-named-pipes">Transactions on Named Pipes</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a>



<a href="/windows/desktop/ipc/pipe-functions">Pipe Functions</a>



<a href="/windows/desktop/ipc/pipes">Pipes Overview</a>



<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe">TransactNamedPipe</a>



<a href="/windows/desktop/api/winbase/nf-winbase-waitnamedpipea">WaitNamedPipe</a>
