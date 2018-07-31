---
UID: NF:winbase.WaitNamedPipeA
title: WaitNamedPipeA function
author: windows-sdk-content
description: Waits until either a time-out interval elapses or an instance of the specified named pipe is available for connection (that is, the pipe's server process has a pending ConnectNamedPipe operation on the pipe).
old-location: base\waitnamedpipe.htm
old-project: ipc
ms.assetid: cbb2300b-5d5f-4a7b-994b-63b747e9ccfc
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: NMPWAIT_USE_DEFAULT_WAIT, NMPWAIT_WAIT_FOREVER, WaitNamedPipe, WaitNamedPipe function, WaitNamedPipeA, WaitNamedPipeW, _win32_waitnamedpipe, base.waitnamedpipe, winbase/WaitNamedPipe, winbase/WaitNamedPipeA, winbase/WaitNamedPipeW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: PRIORITY_HINT
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WaitNamedPipeA function


## -description


Waits until either a time-out interval elapses or an instance of the specified named pipe is available for connection (that is, the pipe's server process has a pending 
<a href="https://msdn.microsoft.com/50f6680f-900e-4411-a849-ec9a911c9e32">ConnectNamedPipe</a> operation on the pipe).


## -parameters




### -param lpNamedPipeName [in]

The name of the named pipe. The string must include the name of the computer on which the server process is executing. A period may be used for the <i>servername</i> if the pipe is local. The following pipe name format is used: 




\\<i>servername</i>\pipe\<i>pipename</i>


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
<a href="https://msdn.microsoft.com/00d79639-3f14-4964-90f3-9462a23e68df">CreateNamedPipe</a> function.

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
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If no instances of the specified named pipe exist, the 
<b>WaitNamedPipe</b> function returns immediately, regardless of the time-out value.

If the time-out interval expires, the <b>WaitNamedPipe</b> function will fail with the error <b>ERROR_SEM_TIMEOUT</b>.

If the function succeeds, the process should use the <a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a> function to open a handle to the named pipe. A return value of <b>TRUE</b> indicates that there is at least one instance of the pipe available. A subsequent <b>CreateFile</b> call to the pipe can fail, because the instance was closed by the server or opened by another client.

<b>Windows 10, version 1709:  </b>Pipes are only supported within an app-container; ie, from one UWP process to another UWP process that's part of the same app. Also, named pipes must use the syntax "\\.\pipe\LOCAL\" for the pipe name.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/0779242c-45f4-4cd9-9c9f-36cff54c8dee">Named Pipe Client</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9cfcb608-a539-4eb6-866c-81dafdabbcdb">CallNamedPipe</a>



<a href="https://msdn.microsoft.com/50f6680f-900e-4411-a849-ec9a911c9e32">ConnectNamedPipe</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a>



<a href="https://msdn.microsoft.com/00d79639-3f14-4964-90f3-9462a23e68df">CreateNamedPipe</a>



<a href="https://msdn.microsoft.com/9e80783e-9641-4cbd-9c28-a8efe6b9efaa">Pipe Functions</a>



<a href="https://msdn.microsoft.com/7cb8cbe4-eec8-4dda-9cb7-8d37abcee6f4">Pipes Overview</a>
 

 

