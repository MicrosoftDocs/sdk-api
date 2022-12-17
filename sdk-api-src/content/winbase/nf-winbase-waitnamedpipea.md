---
UID: NF:winbase.WaitNamedPipeA
title: WaitNamedPipeA function (winbase.h)
description: The WaitNamedPipeA (ANSI) function (winbase.h) waits until either a time-out interval elapses or an instance of the specified named pipe is available for connection (that is, the pipe's server process has a pending ConnectNamedPipe operation on the pipe).
old-location: base\waitnamedpipe.htm
tech.root: ipc
ms.assetid: cbb2300b-5d5f-4a7b-994b-63b747e9ccfc
ms.date: 08/04/2022
ms.keywords: NMPWAIT_USE_DEFAULT_WAIT, NMPWAIT_WAIT_FOREVER, WaitNamedPipe, WaitNamedPipe function, WaitNamedPipeA, WaitNamedPipeW, _win32_waitnamedpipe, base.waitnamedpipe, winbase/WaitNamedPipe, winbase/WaitNamedPipeA, winbase/WaitNamedPipeW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WaitNamedPipeW (Unicode) and WaitNamedPipeA (ANSI)
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
 - WaitNamedPipeA
 - winbase/WaitNamedPipeA
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
 - API-Ms-Win-Core-NamedPipe-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-NamedPipe-Ansi-L1-1-1.dll
 - API-MS-Win-Core-NamedPipe-L1-2-2.dll
api_name:
 - WaitNamedPipe
 - WaitNamedPipeA
 - WaitNamedPipeW
---

# WaitNamedPipeA function


## -description

Waits until either a time-out interval elapses or an instance of the specified named pipe is available for connection (that is, the pipe's server process has a pending 
<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe">ConnectNamedPipe</a> operation on the pipe).

## -parameters

### -param lpNamedPipeName [in]

The name of the named pipe. The string must include the name of the computer on which the server process is executing. A period may be used for the <i>servername</i> if the pipe is local. The following pipe name format is used: 




&#92;&#92;<i>servername</i>\pipe&#92;<i>pipename</i>

### -param nTimeOut [in]

The number of milliseconds that the function will wait for an instance of the named pipe to be available. You can used one of the following values instead of specifying a number of milliseconds. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NMPWAIT_USE_DEFAULT_WAIT"></a><a id="nmpwait_use_default_wait"></a><dl>
<dt><b>NMPWAIT_USE_DEFAULT_WAIT</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The time-out interval is the default value specified by the server process in the 
<a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="NMPWAIT_WAIT_FOREVER"></a><a id="nmpwait_wait_forever"></a><dl>
<dt><b>NMPWAIT_WAIT_FOREVER</b></dt>
<dt>0xffffffff</dt>
</dl>
</td>
<td width="60%">
The function does not return until an instance of the named pipe is available.

</td>
</tr>
</table>

## -returns

If an instance of the pipe is available before the time-out interval elapses, the return value is nonzero.

If an instance of the pipe is not available before the time-out interval elapses, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If no instances of the specified named pipe exist, the 
<b>WaitNamedPipe</b> function returns immediately, regardless of the time-out value.

If the time-out interval expires, the <b>WaitNamedPipe</b> function will fail with the error <b>ERROR_SEM_TIMEOUT</b>.

If the function succeeds, the process should use the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function to open a handle to the named pipe. A return value of <b>TRUE</b> indicates that there is at least one instance of the pipe available. A subsequent <b>CreateFile</b> call to the pipe can fail, because the instance was closed by the server or opened by another client.

<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax `\\.\pipe\LOCAL\` for the pipe name.


#### Examples

For an example, see 
<a href="/windows/desktop/ipc/named-pipe-client">Named Pipe Client</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-callnamedpipea">CallNamedPipe</a>



<a href="/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe">ConnectNamedPipe</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createnamedpipea">CreateNamedPipe</a>



<a href="/windows/desktop/ipc/pipe-functions">Pipe Functions</a>



<a href="/windows/desktop/ipc/pipes">Pipes Overview</a>
