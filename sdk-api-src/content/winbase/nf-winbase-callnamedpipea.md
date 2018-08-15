---
UID: NF:winbase.CallNamedPipeA
title: CallNamedPipeA function
author: windows-sdk-content
description: Connects to a message-type pipe (and waits if an instance of the pipe is not available), writes to and reads from the pipe, and then closes the pipe.
old-location: base\callnamedpipe.htm
old-project: ipc
ms.assetid: 9cfcb608-a539-4eb6-866c-81dafdabbcdb
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CallNamedPipe, CallNamedPipe function, CallNamedPipeA, CallNamedPipeW, NMPWAIT_NOWAIT, NMPWAIT_USE_DEFAULT_WAIT, NMPWAIT_WAIT_FOREVER, _win32_callnamedpipe, base.callnamedpipe, winbase/CallNamedPipe, winbase/CallNamedPipeA, winbase/CallNamedPipeW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: PRIORITY_HINT
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
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
<a href="https://msdn.microsoft.com/00d79639-3f14-4964-90f3-9462a23e68df">CreateNamedPipe</a> function.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the message written to the pipe by the server process is longer than <i>nOutBufferSize</i>, 
<b>CallNamedPipe</b> returns <b>FALSE</b>, and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_MORE_DATA. The remainder of the message is discarded, because 
<b>CallNamedPipe</b> closes the handle to the pipe before returning.




## -remarks



Calling <b>CallNamedPipe</b> is equivalent to calling the <a href="base.createfile">CreateFile</a> (or <a href="https://msdn.microsoft.com/cbb2300b-5d5f-4a7b-994b-63b747e9ccfc">WaitNamedPipe</a>, if <b>CreateFile</b> cannot open the pipe immediately), <a href="https://msdn.microsoft.com/79afcb18-babb-453e-8618-81b43ecb24c4">TransactNamedPipe</a>, and <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> functions. <b>CreateFile</b> is called with an access flag of GENERIC_READ | GENERIC_WRITE, and an inherit handle flag of <b>FALSE</b>.

<b>CallNamedPipe</b> fails if the pipe is a byte-type pipe.

<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax "\\.\pipe\LOCAL\" for the pipe name.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/aedce207-7dea-4670-b6dd-0c61b3f6f690">Transactions on Named Pipes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="base.createfile">CreateFile</a>



<a href="https://msdn.microsoft.com/00d79639-3f14-4964-90f3-9462a23e68df">CreateNamedPipe</a>



<a href="https://msdn.microsoft.com/9e80783e-9641-4cbd-9c28-a8efe6b9efaa">Pipe Functions</a>



<a href="https://msdn.microsoft.com/7cb8cbe4-eec8-4dda-9cb7-8d37abcee6f4">Pipes Overview</a>



<a href="https://msdn.microsoft.com/79afcb18-babb-453e-8618-81b43ecb24c4">TransactNamedPipe</a>



<a href="https://msdn.microsoft.com/cbb2300b-5d5f-4a7b-994b-63b747e9ccfc">WaitNamedPipe</a>
 

 

